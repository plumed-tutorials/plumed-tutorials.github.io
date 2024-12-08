Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1020-777:06283] *** Process received signal ***
[fv-az1020-777:06283] Signal: Aborted (6)
[fv-az1020-777:06283] Signal code:  (-6)
[fv-az1020-777:06283] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1552042520]
[fv-az1020-777:06283] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f15520969fc]
[fv-az1020-777:06283] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1552042476]
[fv-az1020-777:06283] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f15520287f3]
[fv-az1020-777:06283] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f15524a2b9e]
[fv-az1020-777:06283] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f15524ae20c]
[fv-az1020-777:06283] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f15524ae277]
[fv-az1020-777:06283] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f15524ae52b]
[fv-az1020-777:06283] [ 8] plumed(+0x12f48)[0x55c61f9ddf48]
[fv-az1020-777:06283] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1552029d90]
[fv-az1020-777:06283] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1552029e40]
[fv-az1020-777:06283] [11] plumed(+0x131e5)[0x55c61f9de1e5]
[fv-az1020-777:06283] *** End of error message ***
</pre>
{% endraw %}
