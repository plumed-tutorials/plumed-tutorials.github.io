Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[fv-az1778-96:05547] *** Process received signal ***
[fv-az1778-96:05547] Signal: Aborted (6)
[fv-az1778-96:05547] Signal code:  (-6)
[fv-az1778-96:05547] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8890042520]
[fv-az1778-96:05547] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f88900969fc]
[fv-az1778-96:05547] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8890042476]
[fv-az1778-96:05547] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f88900287f3]
[fv-az1778-96:05547] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f88904a2b9e]
[fv-az1778-96:05547] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f88904ae20c]
[fv-az1778-96:05547] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f88904ae277]
[fv-az1778-96:05547] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f88904ae52b]
[fv-az1778-96:05547] [ 8] plumed_master(+0x14254)[0x562a85a1d254]
[fv-az1778-96:05547] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8890029d90]
[fv-az1778-96:05547] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8890029e40]
[fv-az1778-96:05547] [11] plumed_master(+0x14eb5)[0x562a85a1deb5]
[fv-az1778-96:05547] *** End of error message ***
</pre>
{% endraw %}
