Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @67 : keyword ARG is compulsory for this action
[fv-az1429-301:04920] *** Process received signal ***
[fv-az1429-301:04920] Signal: Aborted (6)
[fv-az1429-301:04920] Signal code:  (-6)
[fv-az1429-301:04920] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0b4e242520]
[fv-az1429-301:04920] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f0b4e2969fc]
[fv-az1429-301:04920] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0b4e242476]
[fv-az1429-301:04920] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f0b4e2287f3]
[fv-az1429-301:04920] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f0b4e6a2b9e]
[fv-az1429-301:04920] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f0b4e6ae20c]
[fv-az1429-301:04920] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f0b4e6ae277]
[fv-az1429-301:04920] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f0b4e6ae52b]
[fv-az1429-301:04920] [ 8] plumed_master(+0x14254)[0x562ab832d254]
[fv-az1429-301:04920] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0b4e229d90]
[fv-az1429-301:04920] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0b4e229e40]
[fv-az1429-301:04920] [11] plumed_master(+0x14eb5)[0x562ab832deb5]
[fv-az1429-301:04920] *** End of error message ***
</pre>
{% endraw %}
