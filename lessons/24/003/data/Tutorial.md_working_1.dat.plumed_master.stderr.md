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
[fv-az665-16:69581] *** Process received signal ***
[fv-az665-16:69581] Signal: Aborted (6)
[fv-az665-16:69581] Signal code:  (-6)
[fv-az665-16:69581] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3495e42520]
[fv-az665-16:69581] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3495e969fc]
[fv-az665-16:69581] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3495e42476]
[fv-az665-16:69581] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3495e287f3]
[fv-az665-16:69581] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f34962a2b9e]
[fv-az665-16:69581] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f34962ae20c]
[fv-az665-16:69581] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f34962ae277]
[fv-az665-16:69581] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f34962ae52b]
[fv-az665-16:69581] [ 8] plumed_master(+0x14254)[0x556e3ae7d254]
[fv-az665-16:69581] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3495e29d90]
[fv-az665-16:69581] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3495e29e40]
[fv-az665-16:69581] [11] plumed_master(+0x14eb5)[0x556e3ae7deb5]
[fv-az665-16:69581] *** End of error message ***
</pre>
{% endraw %}
