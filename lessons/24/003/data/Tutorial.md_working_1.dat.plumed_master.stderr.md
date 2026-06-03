Stderr for source:  Tutorial.md_working_1.dat   
Download: [zipped raw stdout](Tutorial.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
A NeighborList is trying to allocate 39 GB of data for the list of neighbors
You can skip this error by exporting "PLUMED_IGNORE_NL_MEMORY_ERROR"
[runnervm3jyl0:47872] *** Process received signal ***
[runnervm3jyl0:47872] Signal: Aborted (6)
[runnervm3jyl0:47872] Signal code:  (-6)
[runnervm3jyl0:47872] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6924c45330]
[runnervm3jyl0:47872] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6924c9eb2c]
[runnervm3jyl0:47872] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6924c4527e]
[runnervm3jyl0:47872] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6924c288ff]
[runnervm3jyl0:47872] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f69250a5ff5]
[runnervm3jyl0:47872] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f69250bb0da]
[runnervm3jyl0:47872] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f69250a5a55]
[runnervm3jyl0:47872] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f69250a5a6f]
[runnervm3jyl0:47872] [ 8] plumed_master(+0x146dd)[0x55f0455e86dd]
[runnervm3jyl0:47872] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6924c2a1ca]
[runnervm3jyl0:47872] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6924c2a28b]
[runnervm3jyl0:47872] [11] plumed_master(+0x15365)[0x55f0455e9365]
[runnervm3jyl0:47872] *** End of error message ***
</pre>
{% endraw %}
