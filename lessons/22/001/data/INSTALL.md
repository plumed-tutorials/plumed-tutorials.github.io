# Requested installation to work with the Funnel Metadynamics (FM)

## Plumed installation
In order to use FM with Plumed it is possible to follow the Plumed tutorial 20.001 "Installing PLUMED" by Tribello G., making sure to add the flag during the configure:
```
--enable-modules=funnel
```
or
```
--enable-modules=all
```

## Third-party applications
FM requires a set of files as input with a well-defined syntax, which might result difficult to to produce for inexperienced user.
For this reason, we have created two ways to automatically create FM inputs:
 * using a tcl plug in, to be used together with the visualization software VMD;
 * a software-free server called Funnel Metadynamics Pre-Processing Tool.

For the former, you will need to download the tooltip library for tcl together with the plug-in file funnel.tcl and load them through the *source* command in the tk terminal of VMD.
The full description of the installation procedure and the links to the necessary code can be found in the paper of the Funnel Metadynamics Advanced Protocol (FMAP) (doi:10.1038/s41596-020-0342-4). Otherwise, the tcl files can be found in the library folder of the [Github](https://github.com/h2nch2co2h/masterclass-22-1.git).

If you wish instead to use the server, there will be no necessity to download the tcl plug in and having a version of VMD installed in your computer.

To be noted that the server still can not run the post-processing analyses, therefore any calculation should either be performed manually by the user (as will be shown in this tutorial) or using the second plug in for VMD ffs.tcl. In this second case, requirements are the same as for funnel.tcl.
