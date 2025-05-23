Stderr for source:  Tutorial.md_working_3.dat   
Download: [zipped raw stdout](Tutorial.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():  std::bad_alloc

The above exception was the direct cause of the following exception:

(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
An error happened while allocating the neighbor list, please decrease the number of atoms used
[pkrvmf6wy0o8zjz:59249] *** Process received signal ***
[pkrvmf6wy0o8zjz:59249] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59249] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59249] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd60ae45330]
[pkrvmf6wy0o8zjz:59249] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd60ae9eb2c]
[pkrvmf6wy0o8zjz:59249] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd60ae4527e]
[pkrvmf6wy0o8zjz:59249] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd60ae288ff]
[pkrvmf6wy0o8zjz:59249] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd60b2a5ff5]
[pkrvmf6wy0o8zjz:59249] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd60b2bb0da]
[pkrvmf6wy0o8zjz:59249] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd60b2a5a55]
[pkrvmf6wy0o8zjz:59249] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd60b2a5a6f]
[pkrvmf6wy0o8zjz:59249] [ 8] plumed_master(+0x146dd)[0x55fa023446dd]
[pkrvmf6wy0o8zjz:59249] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd60ae2a1ca]
[pkrvmf6wy0o8zjz:59249] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd60ae2a28b]
[pkrvmf6wy0o8zjz:59249] [11] plumed_master(+0x15365)[0x55fa02345365]
[pkrvmf6wy0o8zjz:59249] *** End of error message ***
</pre>
{% endraw %}
