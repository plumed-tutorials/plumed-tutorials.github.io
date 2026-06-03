Stderr for source:  Tutorial.md_working_2.dat   
Download: [zipped raw stdout](Tutorial.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
A NeighborList is trying to allocate 39 GB of data for the list of neighbors
You can skip this error by exporting "PLUMED_IGNORE_NL_MEMORY_ERROR"
[runnervm3jyl0:47905] *** Process received signal ***
[runnervm3jyl0:47905] Signal: Aborted (6)
[runnervm3jyl0:47905] Signal code:  (-6)
[runnervm3jyl0:47905] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f07d7e45330]
[runnervm3jyl0:47905] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f07d7e9eb2c]
[runnervm3jyl0:47905] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f07d7e4527e]
[runnervm3jyl0:47905] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f07d7e288ff]
[runnervm3jyl0:47905] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f07d82a5ff5]
[runnervm3jyl0:47905] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f07d82bb0da]
[runnervm3jyl0:47905] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f07d82a5a55]
[runnervm3jyl0:47905] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f07d82a5a6f]
[runnervm3jyl0:47905] [ 8] plumed_master(+0x146dd)[0x5640d6b6a6dd]
[runnervm3jyl0:47905] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f07d7e2a1ca]
[runnervm3jyl0:47905] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f07d7e2a28b]
[runnervm3jyl0:47905] [11] plumed_master(+0x15365)[0x5640d6b6b365]
[runnervm3jyl0:47905] *** End of error message ***
</pre>
{% endraw %}
