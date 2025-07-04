# PLUMED Masterclass 22.2: Analysis of Plumed output by Metadynminer

## Origin

This masterclass was authored by Vojtech Spiwok on February 14, 2022

## Aims

The aim of this Masterclass is to introduce users to the R package Metadynminer for analysis
of results from metadynamics in Plumed.

## Objectives

Once this Masterclass is completed, users will be able to:

- Install R and its packages.
- Load metadynamics results (`HILLS` file) to Metadynminer.
- Calculate a free energy surface and plot it in a publication quality.
- Locate free energy minima and evaluate their relative free energies.
- Make an animation of the evolution of a free energy surface.
- Use data in Metadynminer objects to do advanced calculations (e.g., reweighting).
 
## Setting up the software 

## Installation

We will use [R](https://www.r-project.org/) installed from [CRAN](https://cloud.r-project.org/).
Go to [CRAN](https://cloud.r-project.org/) and follow the installation instructions for your
operating system. R is Open Source. It is not necessary to use a graphical user interface but it
is very useful, especially for making illustrations.

If you plan to use a graphical user interface, the best option is [Rstudio](https://www.rstudio.com/).
[Desktop version of Rstudio](https://www.rstudio.com/products/rstudio/) is Open Source. Follow
the installation instructions for your operating system.

To install metadynminer, open R (in commandline type `R` or open GUI by typing `rstudio` or using
an icon) and type:

````
install.packages("metadynminer")
````

The output should contain: `* DONE (metadynminer)`. If you have an output: `installation of package
metadynminer had non-zero exit status` there was a problem with installation. You may try:

- On MS Windows install `Rtools`.
- If you have permission issues, you can try the commands `Sys.getenv("R_HOME")` and
`Sys.getenv("R_LIBS_USER")` and check the permission of the printed directories. You may change
installation directories by corresponding `Sys.setenv(...)` commands.

You may check whether Metadynminer was installed correctly by typing:

````
library(metadynminer)
````

This command should have no output. Installation is done only once (or can be repreated for
version upgrades). Loading of the package by `library` command must be done in every R seance.

## Resources

The data needed for this Masterclass can be found on [GitHub](https://github.com/plumed/masterclass-22-02).
You can clone this repository using the following command:

````
git clone https://github.com/plumed/masterclass-22-02.git
````

The repository contains hills and colvar files, respectively, from 10 or 1 ns metadynamics simulations of
alanine dipeptide in water calculated in Plumed. Other input data are available from
[Zenodo](https://doi.org/10.5281/zenodo.6056060) but are not required in this tutorial. The repo contains:
- `HILLS.cv12` and `COLVAR.cv12` - hills and collective variable + bias report from metadynamics with phi and psi dihedral angles
- `HILLS.cv1` and `COLVAR.cv1` - hills and collective variable + bias report from metadynamics with phi dihedral angle
- `HILLS.cv2` and `COLVAR.cv2` - hills and collective variable + bias report from metadynamics with psi dihedral angle

This data are independent of Plumed version (for version >=2.0).

## Using R

R is a program and scrpting language predominantly developed for statistical data analysis. It is popular in
statistics, economy, ecology, bioinformatics, and other fields. Let us quickly introduce R. Open R as described
above and type:

```R 
1+1
2-1
3*3
5/2
```

This shows addition, subtraction, multiplication, and division. Numbers and other objects can be saved
to variables. We advice users to avoid the names of variables that can be confused with existing functions
in R. In this masterclass, we will use the prefix "my" (e.g., `myhills`) to avoid this. Variable names are
case-sensitive. The operator used to save something to is an arrow `<-` (less than followed by minus sign).
You may see R codes with a normal equal sign, but we will be puristic in this. Let us show the variables
in R:

```R
x <- 1+1
x
```

In the outputs above, there is an unexpected string `[1]`. This is the index of the first item on the line.
This is useful when dealing with vectors. Vector can be created by implicitly typing its elements to the
function `c()`, by `:` operator and other ways:

```R
x <- c(1, 3, 2)
x
x <- 1:50
x
x <- 50:1
x
```

R can also work with 2D and multidimensional matrices. R can work with strings (written in quotes, e.g.
"blue"), Booleans (`TRUE` and `FALSE`, or shortened as `T` and `F`).

R uses functions written as the name of function followed by its arguments in brackets:

```R
exp(1)
cos(pi)
```

Functions can be applied element-wise:

```R
x<-0:10
cos(x)
```

Functions with more variables use the specifications set by `=`, separated by `,`:

```R
x<-0:100/10
y<-cos(x)
plot(x, y)
plot(x, y, xlab="x axis", ylab="y axis", ylim=c(-2,2))
```

Important difference from many other programming environments is that R can freely change number types,
e.g. `3/2` is evaluated as 1.5, unlike Pyhton, which gives 1, because 3 and 2 are integers,
and not floats.

Another important difference is that R uses indexes of vector items starting with 1 (not 0 line in C/C++,
Python etc.). For example:

```R
x <- c("Carlo", "Gareth", "Giovanni", "Max")
x[2]
\endverbatim
will return Gareth. In contrast, Python returns Giovanni:
\verbatim
x = ["Carlo", "Gareth", "Giovanni", "Max"]
x[2]
```

Finally, R can use other types of objects, including objects defined by a user. Their instances can
be accessed by a string operator. For example, the function `prcomp` performs a principal component
analysis. Its output is an object with multiple instances, for example, with a rotation matrix:

```R
pcamodel <- prcomp(outer(1:3,1:2))
pcamodel
pcamodel$rotation
```

Finally, to quit R you can use the function `q()`. The program asks the user whether he/she wants to
save the data (i.e., variables created in the previous course of the run). We advise users to NOT save
data, i.e. choose the option "n" or function `q(save="n")`. 

## Exercise 1: Calculation of the free energy surface from metadynamics hills

Open R (in Rstudio or command line) and load Metadynminer:

```R
library(metadynminer)
```

Now load the file `HILLS.cv12` into Metadynminer:

```R
myhills12 <- read.hills("HILLS.cv12", per=c(T, T))
```

At this point, it is necessary to set the periodicity of CVs. The free energy surface was calculated using
torsion angles as CVs, which are periodic. It is necessary to set the periodicity to `TRUE` (or simplified
as `T`) as a vector `per`. If you get an error message that the file was not found, it means that
the home directory is not set properly. In Linux command line, the home is the directory where you start
R by the command `R`. In Rstudio, you may navigate to the directory with the file using the File menu
in the right bottom frame. Alternatively, you can use `getwd()` and `setwd("/path/to/your/dir")`.

Hills can be also loaded from a HILLS file posted online by replacing the file name by an URL.

To get help to any function in R, for example, `read.hills`, you can use either `help(read.hills)` or
`?read.hills)`.

If you type the name of the hills file variable `myhills12` you get an information about the number
of hills and CVs. The function `summary` (`summary(myhills12)`) returns the same information plus
the ranges of CVs.

A hills file can be plotted by the `plot` function, i.e., `plot(myhills12)`. For a metadynamics with one
CV it plots the evolution of the CV as a function of time. For a metadynamics with two CVs it plots
a scatter plot with CV1 on the horizontal axis and CV2 on the vertical axis. The plot function applied
on metadynamics hills file is an extension of the standard plot function in R. You may set parameters
`xlab`, `ylab`, `main`, `sub`, `xlim`, `ylim`, `pch`, `col`, `bg`, `cex`, `lwd` and `asp` (see
`?plot.hillsfile`). It is possible to stack plots on top of each other by using the command `plot(...)`,
followed by a command `points(...)` or `lines(...)`.

For well-tempered metadynamics, it may be useful to check the evolution of heights of hills. This
can be done by the command:

```R
plotheights(myhills12)
```

Hills files are often obtained from multiple metadynamics runs. This may cause that time
collumn does not correspond to the real time. The option `ignoretime=T` used either in
`read.hills` or in `plotheights` replaces time by the hill number.

The main point is the calculation of the free energy surface from the hills file as an
negatve image of the sum of Gaussian hills (scaled in well-tempered metadynamics, which
is pre-scaled in the Plumed output).

This may be time consuming with hundreds of thousands of hills. In metadynminer
you can use two functions for this purpose, `fes` and `fes2`. The former is fast and
approximative, the latter is slow and more accurate. The function `fes` uses a pre-computed
Gaussian hill which is simply being shifted on the canvas of the CV space for each hill
and the bias potential is summed. The function `fes2` explicitly evaluates the Gaussian
function. The function `fes` cannot be used in metadynamics with variable hills widths
(the user would be warned).

In our tutorial we can do:

```R
myfes12 <- fes(myhills12)
```

(or the same with `fes2` for analyses, final illustations etc). Typing the name of the
free energy surface variable `myfes12` returns the number of CVs, number of bins
(by default 256 for one CV, and 256x256 for two CVs), free energy maximum and minimum.

It is possible to calculate the value of minimum and maximum of the free energy surface by
functions `min` and `max`, respectively. You may add, subtract, multiply, and divide
the free energy surface by a constant. For example, you can set the free energy
minimum to zero by subtracting the minimum:

```R
myfes12 <- myfes12 - min(myfes12)
```

Similarly, to convert the free energy surface from kJ/mol to kcal/mol you may
divide it by 4.18.

It is also possible to sum and subtract two free energy surfaces. This will be
demonstrated later.

The important function of Metadynaminer is plotting of the free energy surface.
You can use:

```R
plot(myfes12)
```

Again, you may use options `xlim`, `ylim`, `zlim`, `main`, `sub`, `xlab`, `ylab`,
`labcex` and `drawlabels` (see `?plot.fes`). You may control the type of the plot
by the `plottype`. The option `plottype="image"` plots a heat map,
`plottype="contour"` plots contours, and `plottype="both"` plots both. 

It is possible to switch on the free energy scale by:

```R
plot(myfes12, colscale=T)
```

You may change the title of the scale by `colscalelab="your label"`.

It is often necessary to control the levels of contours. For example, to plot
the free energy surface with 20 contours by 10 kJ/mol type:

```R
myfes12 <- myfes12 - min(myfes12)
plot(myfes12, zlim=c(0,200), nlevels=20)
```

You may also explicitly set levels as a vector by the parameter `levels`.

The default color palette for a 2D free energy surface in Metadynminer is
`rainbow(135)[100:1]` (i.e., rainbow without violet color). If you prefer your
own color palette, you may set it as `col` paramtere. For example, this
command plots the free energy surface in gray colors:

```R
plot(myfes12, col=gray.colors(50))
```

Metadynminer can identify minima on the free energy surface. This can be done
by the function:

```R
myminima12 <- fesminima(myfes12)
myminima12
```

The program should find approximately five free energy minima for
alalnine dipeptide in water and print their idetifier (letters A, B, C, ...
followed by AA, AB, AC, ...), location on the free energy
surface (in bin ID and in CVs), and the free energy (for the final
free energy surface). The function `summary` prints also populations
(temperature and energy units can be controlled by `temp` and `eunit`,
respectively).

Some metadynamics simulations may result in rough free energy surfaces with
hundreds of free energy minima. It is not useful to identify all of them.
It is better to find a reasonable number of minima scattered on the whole
free energy surface. The function `fesminima` splits the canvas of the
free energy surface into a certain number of sections (by default 8x8 for 2D and
8 for 1D free energy surfaces, it may be controled by `nbins`). A global minimum
is found in each section and then it is checked whether it is a local minimum
of the entire free energy surface. If not, it is discarded.

It may happen that the function `fesminima` cannot identify some minimum
or it is necessary to add a reference point on a free energy surface, which
is not a minimum. For this purpose, it is possible to make a minimum by
`oneminimum` function and add it to the existing minima (by addition operation).

The output of `fesminima` can be plotted by `plot` function. The plot is
similar to the free energy surface and it contains additional letters in the points
of minima.

```R
plot(myminima12)
```

Convergency of metadynamics can be assessed by the time profile of the differences
between free energy minima. Stable difference between free energy minima indicates
that the free energy surface is converged and thus accurate. It must be kept in
mind that this is a necessary but not the only requirement of convergence.
Please follow the
[PLUMED Masterclass 21.2: Statistical errors in MD ](https://www.plumed.org/doc-v2.7/user-doc/html/masterclass-21-2.html)
for more details. The time profile of the differences between free energy minima
can be caluclated and plotted as:

```R
myprof12 <- feprof(myminima12)
plot(myprof12)
```

The program takes free energy minima (as identified by the function `fesminima`)
and calculates the values of free energy in the same point in the CV space along
the simulation. Typing the name of the time profile returns the same output
as for minima. The function `summary` prints the same output as the summary
of free energy minima together with minimal and maximal free energy relative
to the global free energy minimum. The minimum A is always the global minimum and its
relative free energy is 0 (also its minimum and maximum is zero). The column `tail`
contains the relative free energy at the end of the simulation. It is possible
to specify the time window in which the minimum and maximum are calculated,
for example the second half of the simulation, by `imind` and `imaxd`. By
default they are set to 1 and the number of hills, respectively, i.e. to
whole simulation.

Finally, metadynminer provides a function for the nudged elastic band:

```R
myneb<-neb(myminima12, min1="A", min2="D")
myneb
plot(myneb)
plot(myminima12)
linesonfes(myneb)
```

## Exercise 2: Making high resolution plots and movies

In Rstudio it is possible to save plotted figures in different vector and bitmap formats
and it is possible to customize their resolution. As an alternative, it is possible to
save figures by the functions `png`, `bmp`, `jpeg`, `tiff`, `svg`, `pdf` or `eps`.
These functions use the file name as an argument and it switches the plotting environment,
so that the file is plotted into the file and not on the screen. This option must
be switched off by the function `dev.off()`.
These functions work in the basic R (i.e., without Rstudio) and can be used for
example at high-performance computing clusters, grids, and clouds without GUI.
Our suggestion to make a nice publication quality figure in the size of 8x8 cm
(typical half page) is:

```R
png("filename.png", height=8, width=8, units='cm', res=600, pointsize=6)
plot(myfes12)
dev.off()
```

The functions for image saving can be used with regular expressions. This is
useful for making movies. A movie of free energy evolution can be simply made
by:

```R
tfes<-fes(myhills12, imax=50)
png("snap%04d.png")
plot(tfes, zlim=c(-200,0))
for(i in 1:199) {
  tfes<-tfes+fes(myhills12, imin=50*i+1, imax=50*(i+1))
  plot(tfes, zlim=c(-200,0))
}
dev.off()
```

Functions `imin` and `imax` make it possible to restrict the summation to certain
hill range. The first line calculates the sum of the first 50 hills. The second
call of the `fes` function calculates the sum of hills 51 to 100 and adds it
to the total free energy surface. The resulting 200 files named `snap0001.png`,
`snap0002.png`, etc can be concatenated to a movie by means of some movie
editing software.

## Exercise 3: Making a movie of flooding

The first task in this tutorial is to calculate the free energy surface
of alanine dipeptide calculated in the space of two collective variables
phi and psi. This can be done by typing:

```R
library(metadynminer)
myhills12 <- read.hills("HILLS.cv12", per=c(T, T))
myfes12 <- fes(myhills12)
plot(myfes12)
```

The 2D free energy surface can be converted to 1D by conversion of the free
energy to probability, integration of probabilities along one CV and conversion
back to free energy. In metadynminer you can do this by the function `fes2d21d`:

```R
myfes12.1d <- fes2d21d(myhills12, remdim=2)
```

The option `remdim` sets which CV should be removed (`remdim=2` removes psi).
It is also possible to set the temperature and energy units by `temp` and `eunit`,
respectively.

Now we will use this free energy surface (calculated from 10 ns metadynamics)
as the "ground truth" and we will try how this free energy surface was flooded
by 1 ns metadynamics with a single CV, either phi or psi.

Hills file from the other two simulations can be loaded by:

```R
myhills1 <- read.hills("HILLS.cv1", per=_FILL_)
myhills2 <- read.hills("HILLS.cv2", per=_FILL_)
```

Replace `_FILL_` by the correct expression.

Next, for time 10 ps to 1 ns (hills 10 to 1000, with an increment of 10),
calculate the free energy surface, convert it to a bias potential by
multiplication by minus (biasfactor - 1)/biasfactor and add it to
the ground truth free energy surface. The bias factor was 15 in this
simulation. Plot the result (in black) together with the ground truth
free energy surface in red:

```R
myfes12.1d <- myfes12.1d - min(myfes12.1d)
flooded <- myfes12.1d
flooded$hills <- c()
png("snap%04d.png")
plot(myfes12.1d, ylim=c(0,100), col="red")
for(i in _FILL_) {
  plot(myfes12.1d, ylim=c(0,100), col="red")
  myfes1 <- fes(myhills1, imin=_FILL_, imax=_FILL_)
  flooded <- flooded + _FILL_*myfes1
  lines(flooded)
}
dev.off()
```

Again, replace each `_FILL_` by a suitable expression.
Keep in mind that it is possible to compose the plot from multiple plots.
The function `plot` creates the first plot and functions `lines` or
`points` add to this plot.

The meaning of the line `flooded$hills <- c()` is following.
Objects in R may contain different instances stored as `variable$instance`
The object of the free energy surface contains the free energy surface,
information about the axes and their periodicity and other information,
but also the original hills from which the free energy surface was
calculated. Something similar applies also to the object of free
energy minima. The reason for this is that the function `feprof` needs
hills data. Summation of free energy surfaces is equivalent to
concatenation of hills, so the sum of two free energy surfaces
contains concatenated hills as its `$hills` instance. However,
in the line `flooded <- flooded + _FILL_*myfes1` it is not possible
to concatenate 1D and 2D hills. For this reason we erased hills
from the variable `flooded`.

If possible, make a movie or visually inspect the resulting files.
Evaluate the flooding by the 1D potential in terms of convergence.

## Exercise 4: Reweighing

It would be also interesting to see the performance of metadynamics
with psi torsion as the only CV. Unfortunately, it is not possible to
calculate the free energy surface in the space of phi torsion from this
simulation simply by summing hills. This can be done by reweighing.
This will also demonstrate the advanced features of metadynminer.

Reweighing predicts what would have been the distribution of a CV
or CVs in the biased simulation, if it had not been biased.
[Umbrella sampling reweighing](https://doi.org/10.1016%2F0021-9991%2877%2990121-8)
weights the distribution of the states by
exp(+bias/kT). This can be applied to metadynamics bias
potential with a correction to the time-dependence of the bias
potential. We will use the correction introduced by
[Tiwari and Parrinello](https://doi.org/10.1021/jp504920s).
The main idea is the bias potential is divided into
time-independent and the time-dependent component. The time-dependent
component is calculated by the following procedure:

```R
library(metadynminer)
bf <- 15
nframes <- 50
temp <- 300
myhills2 <- read.hills("HILLS.cv2", per=c(T))
s1<-rep(0, nframes)
s2<-rep(0, nframes)
for(i in 1:nframes) {
  step <- i*length(myhills2$time)/nframes
  onefes <- fes(myhills2, imax=step)
  s1[i] <- sum(exp(-1000*onefes$fes/8.314/temp))
  s2[i] <- sum(exp(-1000*onefes$fes/8.314/temp/bf))
}
ebetac <- s1/s2
```

The variable `bf` contains the bias factor. The R function `rep`
generates a vector by repeating an element. Here it generates
a vector with `nframes` (50) elements equal to zero. The variable
`step` is equal to the number of hills divided by 50 in the first
step, twice as many in the second step, etc. The free energy surface
is calculated for this number of hills. Next, exp(-G/kT) and
exp(-G/kDeltaT) is calculated and stored in vectors `s1` and
`s2`, respectively. Finally, `s1` and `s2` are divided elementwise
and stored to `ebetac`.

Next, we open the colvar file and calculate the probabilities of
the phi torsion. This can be done by:

```R
mycolvar2 <- read.table("COLVAR.cv2")
cv1 <- floor(32*(mycolvar2[,2]+pi)/pi) + 1
bias <- 1000*mycolvar2[,4]
probs <- rep(0, 64)
for(i in 1:nrow(mycolvar2)) {
  step <- (i-1)*nframes/nrow(mycolvar2)+1
  probs[cv1[i]] <- probs[cv1[i]] + exp(bias[i]/temp/8.314)/ebetac[step]
}
fes <- -8.314*temp*log(probs)/1000
fes <- fes - min(fes)
fes[fes>100] <- 100 
myfes <- fes(myhills2, npoints=64, imax=1)
myfes$fes <- fes
plot(myfes, ylim=c(0,60))
```

The function `read.table` is a standard function of R for reading
tabular data. The first CV is extracted from the table and converted
to bin number (with 64 bins). Next, the probability vector `prob` is
generated. The program then runs across all lines of the colvar
file and adds `exp(bias[i]/temp/8.314)/ebetac[step]` to the probability
in the bin of phi angle in i-th line. The resulting probabilities are
converted to free energy and the free energy of unsampled bins
is converted to 100 kJ/mol (instead of infinity, for better handling).
Finally, a free energy surface with 64 bins is calculated from the
first hill and the free energy surface object is replaced by our
`fes`. This free energy surface is plotted. Compare free energy
surfaces calculated with phi CV and psi CV. 
