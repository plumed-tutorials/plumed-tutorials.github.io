# Masterclass 22.01: Funnel Metadynamics (FM): predicting ligand binding models, binding free energies and kinetics

## Origin

This tutorial is a reworked version of the masterclass by Stefano Raniolo and Vittorio Limongelli from the 31st of January, 2022

## Aims

In this tutorial, it will be possible to learn the basics of Funnel Metadynamics (FM), how to set up a FM simulation, and we will see few analyses that are routinely carried out to check for convergence in the calculation. Users might find helpful to read the FM protocol [pubblication](https://www.nature.com/articles/s41596-020-0342-4) in advance.

## Objectives

Once you have completed this tutorial you will be able to:

* Set up a FM simulation using one of the developed tools.
* Use PLUMED and GROMACS to run FM simulations on a paradigmatic system (benzamidine/trypsin).
* Analyse a FM simulation, checking for convergence and calculating the free-energy estimate. It addition these concepts also shown in the Masterclass of 2022, we will also describe a procedure to estimate kinetic constants starting from the information obtained from FM. 

## Recommended PLUMED setup

Although it is possible to use the most basic implementation of PLUMED + GROMACS to follow this tutorial, it is suggested for the user to compile using the MPI library and possibly run the FM simulation on a HPC system.

## Resources

The inputs that are required for the tutorial can in part be found in [Github](https://github.com/h2nch2co2h/masterclass-22-1.git).
You can clone this repository locally in a machine using the following command:

```
git clone https://github.com/h2nch2co2h/masterclass-22-1.git
```

**Simulation of the benzamidine/trypsin system has been carried out with GROMACS v5.14 and a customised version of PLUMED v2.6.**

## Overview of the tutorial

This tutorial can be divided mainly in three main sectors:

* pre-processing: setup of the FM simulation and generation of necessary parameters and inputs;
* simulation: running a FM simulation;
* post-processing: analyse the output of a FM simulation to know thermodynamics and kinetics of a binding mechanism.

We will focalise on the first and last points, leaving running the simulation as a user responsibility.
This is done because a FM simulation can last for days (depending on the hardware where the simulation is being run) if convergence is sought after. In case the user should feel unsure about metadynamics parameters or launching it, it is suggested to follow the this [tutorial](https://www.plumed-tutorials.org/lessons/21/004/data/NAVIGATION.html).
To save up time, we also provide few outputs in case the user would like to skip the simulation phase and directly perform the analyses. 

## Exercises

FM simulations can be run from a correctly minimized and thermalized system and we are giving for granted that the user knows how to perform these tasks. These are the only prerequisite and the tpr file provided is ready for the production run. In case the user would like to apply the following tutorial on a different complex than the benzamidine/trypsin system, we highly recommend to start the pre-processing exercise from a structure that underwent at least minimization and thermalization.

### Pre-processing exercise

The first exercise will be to create a fitting funnel for the system at hand. Similarly to the masterclass, we will use the benzamidine/trypsin system. In general, coordinates and topology for the system should be generated with the MD engine of one's choice, but in this tutorial we are goinge to see examples using GROMACS. You can find coordinates and topology for the benzamidine/trypsin system inside the data folder of Github.

At this point the user can decide to use the VMD plug-in or the Funnel Metadynamics Pre-Processing Tool web-server. We will start here with the former, if you wish to use the latter skip directly to point 18.

1. Open VMD and load the coordinate file (start.gro). In general, this file should be the output at the end of the thermalization process but, in case of neccessity, also a pdb from the Protein DataBank can be used. Go to "Extensions" and press "Tk console". Once the console has been opened you can load the necessary libraries through the following commands:
    ```
    source /path/to/file/tooltip.tcl
    source /path/to/file/funnel.tcl
    ```
    At this point the interface for the FM pre-processing should be accessible by calling in the terminal:
    ```
    funnel_tk
    ```
    or
    ```
    funnel
    ```
    At this point, the GUI should open and an orange funnel should appear in the visualization window.

2. Now it is necessary to adapt the funnel shape, which is initialised with standard values, to the system under study. The first thing to change are the two points that define the axis of the funnel. In the visualization wwindoww of VMD they correspond to two spheres, called A (in yellow) and B (in green). Both points can be modified either by clicking an atom of the system in the visualization window or by changing their Cartesian coordinates in the interface. Starting with point A, select the option to change it from the interface, click on the visualization window of VMD, press the key 'p' and pick an atom of choice of the receptor. The funnel should have changed direction. Do the same for point B. Adjust the funnel axis until you reached a satisfactory coverage of the binding pocket with an acceptable escape pathway. Alternatively, it is possible to change the coordinate boxes of points A and B in the interface by typing a value in Å or using the arrows to increment or decrement their Cartesian coordinates by 0.1 Å. Pressing 'Enter', the value in the box will be read and the funnel will be updated accordingly. During the funnel placement, it is possible to switch between 'Invisible mode' and 'Transparent mode', which could help in better selecting the direction. For the sake of this tutorial coordinates of 4.724, 5.369, and 4.069 nm and 4.597, 5.721, 4.343 nm (for point A and B, respectively) are good enough.

    TO BE NOTED: when using the atom selector with the 'p' key, the system will be constantly waiting for inputs to update point A or B. For this reason, we suggest to always revert to the normal rotation mode of VMD after picking an atom by pressing the 'r' key. This will avoid accidental replacement of point A or B.

3. Next step is to change the funnel shape to adapt to the benzamidine/trypsin system. The 'Zcc' value regulates the switching point between the cone and cylinder region of the funnel and should be selected so that the cone region can include all the residues surrounding the target binding site. Once a value has been selected, press 'Enter' to confirm the change. A value around 1.8 nm should be enough.

    TO BE NOTED: the funnel potential is applied on the center of mass (COM) of the ligand; thus, only the ligand’s COM is kept inside the orange volume during the simulation (large ligands might have part of their structure outside the funnel without feeling any repulsion as long as their COM is within the funnel volume).

4. Together with Zcc, the cone region can be optimised by adjusting the amplitude of the cone section in radians, which is regulated by the 'Alpha' parameter. Greater values increase the explored region of the binding site. Once a value has been selected, press 'Enter' to confirm the change. In this case, a value of 0.55 is a good compromise.

5. Last parameter to fine tune is the 'RCyl', which is the radius of the cylinder section (in the unbound region). The radius value is set by default to 1 Å. In most of the cases, the user does not need to change this value. A larger radius implies a larger volume to explore by the ligand in the unbound state and consequently a more time-consuming calculation. For the tutorial, it is possible to leave the default value but the user can see how the funnel changes increasing the cylinder radius. Always press 'Enter' to finalise the new value.

6. Once the funnel shape has been optimised, it is necessary to limit the sampling of the funnel along the funnel axis and for this we wil use two PLUMED walls. The first is a lower wall 'Low. Wall', which controls the minimum value that can be sampled as projection of the ligand’s COM along the funnel axis. A value of 0 corresponds to the position of point A, with negative values going deeper in the conical region, whereas positive values reduce the sampling to positions closer to the unbound state. A red sphere in the visualization window shows its position relative to points A and B. If the binding mode is not known, 'Low. Wall' should be defined so as to ensure the full exploration of the binding site. A value of -0.3 nm should suffice.

7. The second wall is called 'Up. Wall' and regulates the sampling on the uppermost edge of the funnel, towards the cylinder region. This constraint is set up to accelerate convergence and not waste time in the unbound region. In general, this value should allow for the sampling of 2-3 Å inside the cylinder region outside of the influence of the target (typically from 10 to 15 Å of the closest target atom). It is always computed with respect to the distance from point A and, similarly to 'Low. Wall', it is defined by a red sphere in the visualization window. In our case, anything close to 3.5 nm is sufficient to have an unbound region for benzamidine outside of the trypsin influence.

8. The bias imposed by the FM will be constructed as a grid and, as such, requires lower and upper limits. The lower limit is called 'Min fps.lp' and should be set at least 0.5 Å lower than the value of 'Low. Wall'.

9. Conversely, on the other side we have 'Max fps.lp', which should be set at least 0.5 Å higher than the value of 'Up. Wall'.

10. During the FM simulation it is possible that the simulation might stop due to periodic-boundary-condition issues, which generally missplace the ligand outside of the funnel grid. To counteract this, FM employes an anchor point, which should be an atom of the target structure that is as close as possible to the ligand both in the bound and in the unbound state. To select it, click on the option to define the anchor and then press the key 'p' to select an atom in the visualization window. For the sake of the tutorial, the user can pick whichever atom outside of the trypsin binding pocket.

11. At this point, all necessary parameters for the funnel have been set and we need to define the last parts to complete a working PLUMED input for FM. Type in the box to the right of 'ID' the VMD identification number of the structure you loaded. This number can be found on the left in the VMD main menu where the structure file of the system is loaded.

12. Once the system in VMD has been selected, it is possible to provide a group of atoms that will be used to compute the center of mass (COM) of the ligand using the VMD syntax. Depending on the ligand's structure it could be best to provide a subselection of atoms, but in our example we will just get all heavy atoms of benzamidine by typing:
    ```
    resname MOL and noh
    ```

13. By clicking on 'Apply' a first draft of the PLUMED input should appear, containing all parameters set up until now by the user. It is possible to see few empty variables that must be completed before launching the simulation.

14. This can be done using the drop-down menu. Here, it is possible to select the remaining simulation parameters and type in the box at the right the value for each parameter; press ‘Enter’ and then ‘Apply’ to update the PLUMED input with the new data. We suggest reading the protocol paper for a better description of every single option. In general, all fields with a '<fill>' or '<?>'
flag need to be specified with a user-defined value or file, respectively, before running the simulation.

15. The canvas where the PLUMED input is outputted can also be modified manually, however this should be done as last thing because clicking 'Apply' would reset any manual change.

16. To print the file, it is possible to click on 'Export' and 'Export for Plumed' to create a text file with all the information written in the interface canvas.

    TO BE NOTED: at this point the file is still lacking collective variables (CVs) for the metadynamics. The user should add fitting candidates depending on the system and problem at hand. In our case, a simple distance between the COM of benzamidine and a selection of atoms in the binding pocket of trypsin should suffice.

17. The last step in using the VMD interface involves the creation of a reference pdb file from the target structure used to set up the funnel-shape potential. This file will be used for the alignment of the target structure when the metadynamics bias is added to the system and should be added at the 'REFERENCE' flag in FUNNEL_PS. It should contain only atoms of the target molecule or a selection of them. It is strongly suggested that the backbone atoms of secondary structures (i.e., alpha helix and beta sheet) be chosen.

    TO BE NOTED: beware when creating such a file with VMD since the final structure may have atoms renumbered, and this could create a mismatch during the simulation, causing artifacts and crashes. 

    For users that opted to follow the VMD plug-in route, it is possible to skip directly to the simulation phase. Following, we are going to explain how to use the Funnel Metadynamics Pre-Processing Tool web server.

18. Access the server [website](https://mbuto.si.usi.ch/).

19. Create an account to access the service and log in with the credentials.

20. Create a new 'Discovery' by clicking the plus on the upper left side of the interface and give it a name. This information will remain stored for a certain amount of time in case it is necessary to retrieve the project and change few parameters. Press 'Add' to finalize the creation of the discovery.

21. Load the structure of your interest by fetching a particular PDBID or by uploading the file of your system. The user can click on secondary structures to zoom the view and, by shift+left-clicking, show atoms in a radius of the selected residue. A violet color signals the selected residue and the user can press numbers from 1 to 8 to adjust the zone to display atoms.

22. Start defining the funnel shape by clicking on the funnel icon on the left (named 'Funnel'). A set of options will be displayed on the right, which can be set interactively.

Definition of the parameters follows the same rationale of the VMD plug in (points 1 to 17). Following, we will just specify the procedure.

23. Point A and B can be chosen by clicking on atoms, specifying the value of a given coordinate, or by adapting the value with the arrows in the boxes.

24. Zcc is in the form of a slider, taking as a reference the point A. Alpha and Rcyl can be changed by providing directly a value or with the arrows and they are expressed in radians and Å, respectively.

25. The ANCHOR point is selected by first flagging the checkbox on the left of 'Anchor point' and then clicking on an atom of the interface. Remember to uncheck the box to avoid changing the ANCHOR point by error when the selection is done. When an atom has been selected, its serial number should appear on the right of the option, signaling that an atom has been correctly provided.

26. It is possible to undisplay or display the Funnel by clicking on the eye on the top right of the interface. 

27. Switch to the 'Bounds' section on the left panel to start defining the walls and upper and lower limits that will be applied in the FM simulation.

28. In the web server, the walls and limits are defined with sliders and they are represented by discs, clearly defining their boundaries with respect to point A. The web server has also an internal check to warn the user if improper values of bounds have been selected. In this case, a red message will be displayed on the side of the wrong parameter.

29. A new feature of the web server is the possibility to define geometric collective variables that can be added directly in the PLUMED input at the end of the procedure. To do so, switch to the 'Collective variables' panel on the left that has a wrench as symbol.

30. A list of user-defined collective variables can be found on the upper right of the interface. To date, it is possible to set a distance, angle, or dihedral angle and the system will automatically recognize the type of CV based on the user interaction. By right-clicking with the mouse on atoms the system will start to store their information and right-clicking again on the same atom stops the procedure. Thus, if the user right-clicks on two atoms and stops the selection there by right-clicking again on the second atom, a distance will be defined.

31. It is also possible to define centers of mass (COM) to be used with the geometrical CVs. To do so, check the box on the left of CV virtual Atom and start selecting atoms with the left-click of the mouse. A red sphere should show the position of the COM in the Cartesian space and it updates for each new selection. When the user is satisfied in selecting the correct number of atoms, a click on the plus on the right of the interface finalizes the selection and stops the process to start a new COM definition.

32. A 'History Log' is accessible on the left panel by clicking on the homonymous option (clock symbol). Here the user can revert a move or restore a previous state in the definition of parameters.

33. Once all the parameters have been set, it is possible to create the PLUMED input file. To do so, click on the 'Protein' option at the top of the left panel (symbolized by atoms) and click on the 'PLUMED FILE' button on the right of the interface. A window should pop up with boxes to define the final values to complete the input and a drop-down menu to select particular CVs if any have been defined. It is also possible to create the pdb file to provide to the REFERENCE flag in FUNNEL_PS, although we suggest the user to adapt this file to the system under study as explained in the reference [protocol](https://www.nature.com/articles/s41596-020-0342-4).

34. Press the 'DOWNLOAD' button to obtain a PLUMED input file.

The procedure of pre-processing is now terminated and the user can progress to the Simulation phase. In case of bugs, please contact the email address andreabritesma@gmail.com.


### Simulation

This part of the tutorial is elective and, depepnding on the system under study and hardware, it could require some simulation time.
For this reason, we provide files that could be used by the user to skip directly to the post-processing exercise. 

For the following exercise, we are going to use GROMACS.

1. To launch a FM simulation, launch a normal simulation in GROMACS adding the flag '-plumed' followed by the name of the file prepared in the pre-processing exercise. Depending on the version and configuration of GROMACS in your machine, the command input might slightly change.

    For GROMACS-5.1.4+PLUMED-2.6:
    ```GROMACS-5.1.4+PLUMED-2.6
    mdrun -deffnm runme -plumed namefile.dat
    ```
    For GROMACS-2020.6+PLUMED-2.7.1 (serial version):
    ```GROMACS-2020.6+PLUMED-2.7.1 (serial version)
    gmx mdrun -deffnm runme -plumed namefile.dat
    ```
    For GROMACS-2020.6+PLUMED-2.7.1 (MPI version):
    ```GROMACS-2020.6+PLUMED-2.7.1 (MPI version)
    mpirun -np X gmx_mpi mdrun -deffnm runme -plumed namefile.dat
    ```

2. Check that the files 'HILLS', 'COLVAR' and 'BIAS' are created. The 'BIAS' file contains the information of the funnel-shape restraint potential.

3. Stop the FM simulation once the free-energy calculation reaches convergence. To check the convergence, compute the binding free-energy surface (BFES) as a function of the simulation time. This operation can be done while the simulation is ongoing using the command:
    ```
    plumed --no-mpi sum_hills --hills HILLS --mintozero --stride X
    ```
    As a rule of thumb, the calculation is converged if the system continues exploring the bound and unbound state in the CV space, while the computed BFES as a function of the time does not change significantly. 
    
    TO BE NOTED: the simulation time to converge in the calculation is variable and depends on several factors, such as the size of the system, the number and types of CVs and metadynamics parameters. In the case of benzamidine–trypsin, the calculation converged after 250 ns. This check can be done with the help of the post-processing interface if necessary (see point X in post-processing exercise).

### Post-processing exercise

In case the user did not run the simulation, we provide sample files start.pdb and trj.trr to load a strided FM simulation, the HILLS file of the simulation, a number of binding free-energy surfaces (BFES), and a COLVAR file already strided.

The user can follow the procedure through the following numbered points and the graphical user interface FFS. Additionally, a notebook (Solution.ipynb) is provided in the github folder, which contains the most important calculations inside the tool.

1. Open VMD and load the trajectory produced by the simulation in the Simulation exercise. This can be done by loading xtc + gro, or crd + prmtop, or dcd + pdb files for example (users will find start.pdb and trj.trr in data/post-processing).

2. Source the plug-in ffs.tcl to start the analysis of the FM trajectory. To do so, go to Extension->Tk console on the Main window of VMD, type
    ```
    source /path/to/file/ffs.tcl
    ```
    and then
    ```
    ffs_tk
    ```
    The post-processing GUI should now be visible. 

    TO BE NOTED: in case the tooltip library was not loaded beforehand, please follow indications in point 1 of the pre-processing exercise before sourcing ffs.tcl.

    Two post-processing calculations are available. The first allows the calculation of the BFES through the PLUMED-2 'sum_hills' command. This is used for one of the convergence checks routinely done on metadynamics calculations and to reconstruct the BFES as a function of the CVs used in the simulation.
    The second option uses the PLUMED-2 'driver' command to provide values of CVs, rescale potentials, and much more along the simulation trajectory.
    We will start describing the first option. You can find the second option from point 9.

3. Click the 'Plumed (bin)' button and select the folder path to the binary file 'plumed' of PLUMED-2 on the user’s computer. The name of the selected file is shown to the right of the button.

4. Click the 'Hills' button and select the folder path to the 'HILLS' file produced in Step 1 of the 'Simulation' phase. Alternatively, the user can load the HILLS_800ns provided inside the github folder.

5. Decide whether to use the lowest energy minimum as the ground state (0 kJ/mol state) through the ‘Min to zero?’ drop-down menu. This operation facilitates the comparison between states and has no consequence on the computation of the BFES.

6. Specify the value of the product between the Boltzmann constant and the temperature in kJ/mol (e.g., 2.479 at 298 K).

7. Click the ‘Output’ button and select the folder in which you prefer to save the output files. The folder name appears to the right of the button.

8. Click 'RUN Sum_hills LR' to compute the BFES using a small bin number (150 points per CV). This is recommended to avoid computer cache memory issues when plotting the BFES in the FMAP GUI (Step 16). Alternatively, click 'RUN Sum_hills HR' to compute the BFES using a larger bin number, which is useful for the accurate estimate of the ligand binding free energy (Step 19). You can produce several BFESs computed along the simulation time by clicking 'RUN Sum_hills stride'. The number of BFESs produced depends on the stride value specified in the 'stride' entry. 'RUN Sum_hills stride' is useful for the convergence control and the binding free-energy calculation (Step 20). In all the cases, wait until the calculation is complete. The output of sum_hills is displayed in the VMD tk console; thus, you can check the progress of the calculation.

    Alternatively, you can use the interface to perform a driver calculation. Skip to step 16 to continue the analysis of the BFESs.

9. Click the ‘Plumed (bin)’ button and select the folder path to the binary file 'plumed' of PLUMED-2 on the user’s computer. The name of the selected file is shown to the right of the button.

10. Prepare a PLUMED-2 input file using a text editor and specify the CVs for which the statistics along the simulation should be computed. To load the file, click the 'Input (.dat)' button. The name of the selected file is shown to the right of the button.

11. Click the 'Trajectory' button to select the trajectory on which the Driver command should run.

    TO BE NOTED: the full (not strided) trajectory of the simulation produced at Step 1 of the 'Simulation' phase should be used.

12. Specify the trajectory format depending on the program used for the FM simulation (i.e., .xtc or .trr for GROMACS, .dcd for NAMD and .crd for Amber, respectively) by using the drop-down menu to the right of 'Trajectory extension'.

13. Click the 'Pdb file' button and specify the .pdb file of the system associated to the trajectory. In this file, the occupancy and beta-factor columns should be replaced with the mass and charge of each atom, respectively, especially if the collective variable (CV) computed employs calculations dependent on either of them.

14. Click the 'Output' button and select the folder in which you prefer to save the output files.

15. Click 'RUN Driver' and wait until the calculation is completed. The calculation output of driver is displayed in the VMD tk console, allowing you to check the progress of the calculation.

16. Plot the BFES of the system using the ‘Plot FES’ button. You can plot the BFES created at Step 8 or any other FES in the PLUMED-2 format. You can plot both 1D and 2D FESs. As reported in Step 8, for this task we recommend creating the FES using 'RUN Sum_hills LR' to avoid computer cash memory issues.

17. The user can scroll the frames of the simulation trajectory loaded at Step 11 and visualize at the same time their position in the BFES produced at Step 25 by clicking the 'Trace' button. To make this option active, click 'Output' and select the folder path to the 'COLVAR' file. The COLVAR file should have the same number of frames of the simulation trajectory. To ensure this is
the case, if you have not already, create the COLVAR file from the trajectory loaded in VMD using 'Driver' as shown from step 9 to 15. Otherwise, a COLVAR file with the same number of frames of trj.trr is provided in the github folder.

18. You can extract the system structures belonging to a selected region in the BFES (i.e., the binding poses at the lowest free-energy minimum). To do so, click 'Output' and specify the folder path to the 'COLVAR' file that has the same number of frames of the trajectory. If the file is missing, follow Step 9 to create a new 'COLVAR' file. Then, hold the right button of the mouse drawing a selection area in the displayed BFES (depending on your OS the keybind might change). A pop-up message is displayed to inform the user about the number of structures that will be extracted. A new folder called 'Selected_structures' is automatically created including the pdb file for each frame extracted. The pdb files are named after the frame number, and a log file reports the list of frame numbers that were extracted. Alternatively, the same result is obtained by typing the CV interval of interest in the FES in the boxes to the right ('min_x' 'max_x'; 'min_y' 'max_y') and clicking 'Extract'. If the displayed FES is 1D, use only the first two boxes ('min_x' and 'max_x'); in the case of 2D FESs, all four fields should be filled ('min_x', 'max_x', 'min_y' and 'max_y').

19. Calculate the absolute protein–ligand binding free energy. To do so, first type the CV interval identifying the bound state in the boxes introduced at Step 18 ('min_x' and 'max_x' in the case of 1D BFES; 'min_x', 'max_x', 'min_y' and 'max_y' in the case of 2D BFES). Looking at the BFES, type in 'Wref value at' the reference CV value for the unbound state (i.e., the ligand is far from the protein and the BFES is flat). Specify the radius of the cylinder section used during the FM simulation and click 'Calculate!'. The GUI will ask for a BFES file for the calculation. You can provide either the BFES generated by 'RUN Sum_hills LR' at Step 8 or a
new BFES calculated by clicking 'RUN Sum_hills HR', which might lead to a more accurate estimate of the ligand binding free energy. Unlike when executing the previous commands, the calculation output is not displayed in the VMD terminal; instead, the final value is
shown in kcal/mol to the right of the 'Calculate!' button. This estimate already includes the entropy correction due to the presence of the funnel-shape potential.

20. The user can compute the ligand binding free energy and its standard deviation as a function of the simulation time. This operation is useful to assess the convergence of the FM calculation. Practically, the ligand binding free energy and its s.d. are estimated generating several BFESs computed as time-weighted average along the simulation. The BFES files can be created in Step 8. Select the folder where all the BFESs are stored by clicking the 'Output' button. Type the CV interval identifying the bound state and the reference CV value for the unbound state as done in Step 18. Finally, type the radius of the cylinder section used during the FM simulation and click 'Convergence'. At the end of the job, a graph of the binding free-energy difference as a function of the serial number of BFES is displayed. At the same time, the value of the freeenergy difference with the corresponding s.d. computed from each BFES is reported in the tk_console of VMD.

21. At the beginning of the simulation, the free-energy calculation has not converged yet; therefore, the graph obtained in Step 20 typically shows large fluctuations. The user can exclude this part of the simulation from the computation of the graph in Step 20 by typing the number of frames to discard in the field on the right of 'Rej. Time' (reject time). Then, repeat Step 20 to recompute the
ligand binding free energy and its s.d. without considering the initial part of the simulation. The 'Rej. Time' can be easily defined by looking at the graph generated in Step 20 and identifying the converged part in the binding free-energy graph that shows lower fluctuations around a given value.

22. In addition to Step 21, the user can check the convergence of the FM calculation through a block bootstrap analysis performed by clicking the button 'Block bootstrap'. Once you have defined the 'Rej. Time' as shown in Step 21, the remaining simulation frames are divided in ten blocks, and for each of them a bootstrap analysis is performed. The user obtains the estimation of the mean of
the binding free energy and its standard error and a histogram representation of the values distribution for each block. The user should check that the distributions are Gaussian like. The convergence of the calculation is reached when the values of the binding free energy computed in the last blocks are very close (i.e., their difference is <1 kcal/mol). We note that the binding free-energy value computed in the last block should be very similar to that computed in Step 21.

At this point the user should have achieved convergence and the value provided from the last point in the weighted avergae can be reported as the result of FM for the system under study.
