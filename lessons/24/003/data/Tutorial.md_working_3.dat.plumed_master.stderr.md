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
[fv-az1778-96:05230] *** Process received signal ***
[fv-az1778-96:05230] Signal: Aborted (6)
[fv-az1778-96:05230] Signal code:  (-6)
[fv-az1778-96:05230] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3dac842520]
[fv-az1778-96:05230] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3dac8969fc]
[fv-az1778-96:05230] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3dac842476]
[fv-az1778-96:05230] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3dac8287f3]
[fv-az1778-96:05230] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f3dacca2b9e]
[fv-az1778-96:05230] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f3daccae20c]
[fv-az1778-96:05230] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f3daccae277]
[fv-az1778-96:05230] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f3daccae52b]
[fv-az1778-96:05230] [ 8] plumed_master(+0x14254)[0x55df60359254]
[fv-az1778-96:05230] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3dac829d90]
[fv-az1778-96:05230] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3dac829e40]
[fv-az1778-96:05230] [11] plumed_master(+0x14eb5)[0x55df60359eb5]
[fv-az1778-96:05230] *** End of error message ***
</pre>
{% endraw %}
