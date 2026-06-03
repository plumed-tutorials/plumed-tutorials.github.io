# Flamegraph with perf from plumed benchmark

Flamegraphs provide you with a way for visualising how long is spent in each of the functions that make up a large piece of software like PLUMED.  Constructing these graphs is a useful way to 
identify bottlenecks in codes and ways of optimising your calculations.

The best way to understand how to create a flame graph is by looking at the [original site](https://www.brendangregg.com/FlameGraphs/cpuflamegraphs.html).
A step-by-step instruction guide can be found on that site (this step by step guide is for linux.  Mac OS user can follow some links [here](https://www.brendangregg.com/flamegraphs.html)):

Before working through the step by step guides above you should:
- ensure you have enough permission to run processes with perf
- recompile plumed with `CXXFLAGS='-O3 -g -fno-omit-frame-pointer' CFLAGS="-g -O2 -fno-omit-frame-pointer" ./configure other options` [-fno-omit-frame-pointer](https://www.brendangregg.com/FlameGraphs/cpuflamegraphs.html#C) is necessary on linux to correctly time the functions (you can use also `-gdwarf` instead of `-g`)
    - do the same also with all the kernels you want to measure
- clone the repository `git clone https://github.com/brendangregg/FlameGraph.git`, or download the release
    - save the path of the repository (I saved it as `flameDir`)
- run the benchmark with perf:
```bash
perf record -F99 --call-graph dwarf --output="benchmark-school-perf.data" \
    plumed benchmark --natoms=1000 --nsteps=50 --atom-distribution=sc > perf.out
```
- then post process with perf :
```bash
perf script --input=benchmark-school-perf.data > benchmark-school-perf.perf
```
- before you post process with the flamegraphs utilities:
```bash
"${flameDir}"/FlameGraph/stackcollapse-perf.pl benchmark-school-perf.perf > benchmark-school-perf.folded 
"${flameDir}"/FlameGraph/flamegraph.pl benchmark-school-perf.folded > benchmark-school-perf.svg
```
You can then open the flamegraph.  You should see something similar to the graph shown below.

![](benchmark-school-perf.svg)


When reading a flame graph remember: the functions are horizontally in alphabetical order.
The horizontal space is the percent of time that the function occupies in time and the height of the rectangle is the stack depth in which that function has been measured.

For example in the column on the right where the base is "_start" you can see that of all the functions calls in the stack of "mca_base*" basically all the time is occupied by the "do_lookup_x" on the top of that stack.

If you open the svg with a browser you can click on the individual functions to zoom in. There is also a search utility when the graph is opened with a browser.
