Stderr for source:  Tutorial.md_working_3.dat   
Download: [zipped raw stdout](Tutorial.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
A NeighborList is trying to allocate 39 GB of data for the list of neighbors
You can skip this error by exporting "PLUMED_IGNORE_NL_MEMORY_ERROR"
[runnervm3jyl0:47936] *** Process received signal ***
[runnervm3jyl0:47936] Signal: Aborted (6)
[runnervm3jyl0:47936] Signal code:  (-6)
[runnervm3jyl0:47936] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f759fc45330]
[runnervm3jyl0:47936] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f759fc9eb2c]
[runnervm3jyl0:47936] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f759fc4527e]
[runnervm3jyl0:47936] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f759fc288ff]
[runnervm3jyl0:47936] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f75a00a5ff5]
[runnervm3jyl0:47936] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f75a00bb0da]
[runnervm3jyl0:47936] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f75a00a5a55]
[runnervm3jyl0:47936] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f75a00a5a6f]
[runnervm3jyl0:47936] [ 8] plumed_master(+0x146dd)[0x55d1ec5da6dd]
[runnervm3jyl0:47936] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f759fc2a1ca]
[runnervm3jyl0:47936] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f759fc2a28b]
[runnervm3jyl0:47936] [11] plumed_master(+0x15365)[0x55d1ec5db365]
[runnervm3jyl0:47936] *** End of error message ***
</pre>
{% endraw %}
