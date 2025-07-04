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
[pkrvmbietmlfzoi:35536] *** Process received signal ***
[pkrvmbietmlfzoi:35536] Signal: Aborted (6)
[pkrvmbietmlfzoi:35536] Signal code:  (-6)
[pkrvmbietmlfzoi:35536] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f389f245330]
[pkrvmbietmlfzoi:35536] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f389f29eb2c]
[pkrvmbietmlfzoi:35536] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f389f24527e]
[pkrvmbietmlfzoi:35536] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f389f2288ff]
[pkrvmbietmlfzoi:35536] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f389f6a5ff5]
[pkrvmbietmlfzoi:35536] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f389f6bb0da]
[pkrvmbietmlfzoi:35536] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f389f6a5a55]
[pkrvmbietmlfzoi:35536] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f389f6a5a6f]
[pkrvmbietmlfzoi:35536] [ 8] plumed_master(+0x146dd)[0x5629e63ba6dd]
[pkrvmbietmlfzoi:35536] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f389f22a1ca]
[pkrvmbietmlfzoi:35536] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f389f22a28b]
[pkrvmbietmlfzoi:35536] [11] plumed_master(+0x15365)[0x5629e63bb365]
[pkrvmbietmlfzoi:35536] *** End of error message ***
</pre>
{% endraw %}
