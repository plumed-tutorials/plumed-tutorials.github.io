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
[pkrvmbietmlfzoi:35568] *** Process received signal ***
[pkrvmbietmlfzoi:35568] Signal: Aborted (6)
[pkrvmbietmlfzoi:35568] Signal code:  (-6)
[pkrvmbietmlfzoi:35568] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa60ba45330]
[pkrvmbietmlfzoi:35568] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa60ba9eb2c]
[pkrvmbietmlfzoi:35568] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa60ba4527e]
[pkrvmbietmlfzoi:35568] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa60ba288ff]
[pkrvmbietmlfzoi:35568] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa60bea5ff5]
[pkrvmbietmlfzoi:35568] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa60bebb0da]
[pkrvmbietmlfzoi:35568] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa60bea5a55]
[pkrvmbietmlfzoi:35568] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa60bea5a6f]
[pkrvmbietmlfzoi:35568] [ 8] plumed_master(+0x146dd)[0x55d37f56d6dd]
[pkrvmbietmlfzoi:35568] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa60ba2a1ca]
[pkrvmbietmlfzoi:35568] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa60ba2a28b]
[pkrvmbietmlfzoi:35568] [11] plumed_master(+0x15365)[0x55d37f56e365]
[pkrvmbietmlfzoi:35568] *** End of error message ***
</pre>
{% endraw %}
