Stderr for source:  MultiColvar.md_working_4.dat   
Download: [zipped raw stdout](MultiColvar.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1535-978:69546] *** Process received signal ***
[fv-az1535-978:69546] Signal: Aborted (6)
[fv-az1535-978:69546] Signal code:  (-6)
[fv-az1535-978:69546] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff142042520]
[fv-az1535-978:69546] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff1420969fc]
[fv-az1535-978:69546] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff142042476]
[fv-az1535-978:69546] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff1420287f3]
[fv-az1535-978:69546] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff1424a2b9e]
[fv-az1535-978:69546] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff1424ae20c]
[fv-az1535-978:69546] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff1424ae277]
[fv-az1535-978:69546] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff1424ae52b]
[fv-az1535-978:69546] [ 8] plumed(+0x12f48)[0x5578a92b3f48]
[fv-az1535-978:69546] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff142029d90]
[fv-az1535-978:69546] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff142029e40]
[fv-az1535-978:69546] [11] plumed(+0x131e5)[0x5578a92b41e5]
[fv-az1535-978:69546] *** End of error message ***
</pre>
{% endraw %}
