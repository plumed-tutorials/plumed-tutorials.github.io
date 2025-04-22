Stderr for source:  Tutorial.md_working_1.dat   
Download: [zipped raw stdout](Tutorial.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():  std::bad_alloc

The above exception was the direct cause of the following exception:

(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
An error happened while allocating the neighbor list, please decrease the number of atoms used
[fv-az2211-783:06416] *** Process received signal ***
[fv-az2211-783:06416] Signal: Aborted (6)
[fv-az2211-783:06416] Signal code:  (-6)
[fv-az2211-783:06416] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fae1f245330]
[fv-az2211-783:06416] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fae1f29eb2c]
[fv-az2211-783:06416] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fae1f24527e]
[fv-az2211-783:06416] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fae1f2288ff]
[fv-az2211-783:06416] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fae1f6a5ff5]
[fv-az2211-783:06416] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fae1f6bb0da]
[fv-az2211-783:06416] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fae1f6a5a55]
[fv-az2211-783:06416] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fae1f6a5a6f]
[fv-az2211-783:06416] [ 8] plumed_master(+0x146dd)[0x55ca8fd1c6dd]
[fv-az2211-783:06416] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fae1f22a1ca]
[fv-az2211-783:06416] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fae1f22a28b]
[fv-az2211-783:06416] [11] plumed_master(+0x15365)[0x55ca8fd1d365]
[fv-az2211-783:06416] *** End of error message ***
</pre>
{% endraw %}
