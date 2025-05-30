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
[pkrvmf6wy0o8zjz:59487] *** Process received signal ***
[pkrvmf6wy0o8zjz:59487] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59487] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59487] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbcbfc45330]
[pkrvmf6wy0o8zjz:59487] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbcbfc9eb2c]
[pkrvmf6wy0o8zjz:59487] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbcbfc4527e]
[pkrvmf6wy0o8zjz:59487] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbcbfc288ff]
[pkrvmf6wy0o8zjz:59487] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbcc00a5ff5]
[pkrvmf6wy0o8zjz:59487] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbcc00bb0da]
[pkrvmf6wy0o8zjz:59487] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbcc00a5a55]
[pkrvmf6wy0o8zjz:59487] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbcc00a5a6f]
[pkrvmf6wy0o8zjz:59487] [ 8] plumed_master(+0x146dd)[0x55b2ad2076dd]
[pkrvmf6wy0o8zjz:59487] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbcbfc2a1ca]
[pkrvmf6wy0o8zjz:59487] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbcbfc2a28b]
[pkrvmf6wy0o8zjz:59487] [11] plumed_master(+0x15365)[0x55b2ad208365]
[pkrvmf6wy0o8zjz:59487] *** End of error message ***
</pre>
{% endraw %}
