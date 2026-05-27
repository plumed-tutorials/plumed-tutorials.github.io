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
[runnervm3jyl0:80389] *** Process received signal ***
[runnervm3jyl0:80389] Signal: Aborted (6)
[runnervm3jyl0:80389] Signal code:  (-6)
[runnervm3jyl0:80389] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe015845330]
[runnervm3jyl0:80389] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe01589eb2c]
[runnervm3jyl0:80389] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe01584527e]
[runnervm3jyl0:80389] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe0158288ff]
[runnervm3jyl0:80389] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe015ca5ff5]
[runnervm3jyl0:80389] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe015cbb0da]
[runnervm3jyl0:80389] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe015ca5a55]
[runnervm3jyl0:80389] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe015ca5a6f]
[runnervm3jyl0:80389] [ 8] plumed_master(+0x146dd)[0x563027e8a6dd]
[runnervm3jyl0:80389] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe01582a1ca]
[runnervm3jyl0:80389] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe01582a28b]
[runnervm3jyl0:80389] [11] plumed_master(+0x15365)[0x563027e8b365]
[runnervm3jyl0:80389] *** End of error message ***
</pre>
{% endraw %}
