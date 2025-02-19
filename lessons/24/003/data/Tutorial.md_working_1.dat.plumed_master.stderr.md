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
[fv-az1690-151:06635] *** Process received signal ***
[fv-az1690-151:06635] Signal: Aborted (6)
[fv-az1690-151:06635] Signal code:  (-6)
[fv-az1690-151:06635] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fccc1a45330]
[fv-az1690-151:06635] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fccc1a9eb2c]
[fv-az1690-151:06635] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fccc1a4527e]
[fv-az1690-151:06635] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fccc1a288ff]
[fv-az1690-151:06635] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fccc1ea5ff5]
[fv-az1690-151:06635] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fccc1ebb0da]
[fv-az1690-151:06635] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fccc1ea5a55]
[fv-az1690-151:06635] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fccc1ea5a6f]
[fv-az1690-151:06635] [ 8] plumed_master(+0x146dd)[0x55894dfe46dd]
[fv-az1690-151:06635] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fccc1a2a1ca]
[fv-az1690-151:06635] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fccc1a2a28b]
[fv-az1690-151:06635] [11] plumed_master(+0x15365)[0x55894dfe5365]
[fv-az1690-151:06635] *** End of error message ***
</pre>
{% endraw %}
