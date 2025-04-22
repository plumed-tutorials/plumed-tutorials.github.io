Stderr for source:  Tutorial.md_working_2.dat   
Download: [zipped raw stdout](Tutorial.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Tutorial.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():  std::bad_alloc

The above exception was the direct cause of the following exception:

(tools/NeighborList.cpp:117) void PLMD::NeighborList::initialize()
An error happened while allocating the neighbor list, please decrease the number of atoms used
[fv-az2211-783:06450] *** Process received signal ***
[fv-az2211-783:06450] Signal: Aborted (6)
[fv-az2211-783:06450] Signal code:  (-6)
[fv-az2211-783:06450] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2377645330]
[fv-az2211-783:06450] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f237769eb2c]
[fv-az2211-783:06450] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f237764527e]
[fv-az2211-783:06450] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f23776288ff]
[fv-az2211-783:06450] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2377aa5ff5]
[fv-az2211-783:06450] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2377abb0da]
[fv-az2211-783:06450] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2377aa5a55]
[fv-az2211-783:06450] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2377aa5a6f]
[fv-az2211-783:06450] [ 8] plumed_master(+0x146dd)[0x5557747646dd]
[fv-az2211-783:06450] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f237762a1ca]
[fv-az2211-783:06450] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f237762a28b]
[fv-az2211-783:06450] [11] plumed_master(+0x15365)[0x555774765365]
[fv-az2211-783:06450] *** End of error message ***
</pre>
{% endraw %}
