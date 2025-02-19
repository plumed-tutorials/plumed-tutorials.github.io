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
[fv-az1690-151:06666] *** Process received signal ***
[fv-az1690-151:06666] Signal: Aborted (6)
[fv-az1690-151:06666] Signal code:  (-6)
[fv-az1690-151:06666] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9b0aa45330]
[fv-az1690-151:06666] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9b0aa9eb2c]
[fv-az1690-151:06666] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9b0aa4527e]
[fv-az1690-151:06666] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9b0aa288ff]
[fv-az1690-151:06666] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9b0aea5ff5]
[fv-az1690-151:06666] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9b0aebb0da]
[fv-az1690-151:06666] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9b0aea5a55]
[fv-az1690-151:06666] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9b0aea5a6f]
[fv-az1690-151:06666] [ 8] plumed_master(+0x146dd)[0x56282909d6dd]
[fv-az1690-151:06666] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9b0aa2a1ca]
[fv-az1690-151:06666] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9b0aa2a28b]
[fv-az1690-151:06666] [11] plumed_master(+0x15365)[0x56282909e365]
[fv-az1690-151:06666] *** End of error message ***
</pre>
{% endraw %}
