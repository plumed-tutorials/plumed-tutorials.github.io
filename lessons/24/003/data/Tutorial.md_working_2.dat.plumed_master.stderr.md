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
[fv-az665-16:69603] *** Process received signal ***
[fv-az665-16:69603] Signal: Aborted (6)
[fv-az665-16:69603] Signal code:  (-6)
[fv-az665-16:69603] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa1e9442520]
[fv-az665-16:69603] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa1e94969fc]
[fv-az665-16:69603] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa1e9442476]
[fv-az665-16:69603] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa1e94287f3]
[fv-az665-16:69603] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa1e98a2b9e]
[fv-az665-16:69603] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa1e98ae20c]
[fv-az665-16:69603] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa1e98ae277]
[fv-az665-16:69603] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa1e98ae52b]
[fv-az665-16:69603] [ 8] plumed_master(+0x14254)[0x563211feb254]
[fv-az665-16:69603] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa1e9429d90]
[fv-az665-16:69603] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa1e9429e40]
[fv-az665-16:69603] [11] plumed_master(+0x14eb5)[0x563211febeb5]
[fv-az665-16:69603] *** End of error message ***
</pre>
{% endraw %}
