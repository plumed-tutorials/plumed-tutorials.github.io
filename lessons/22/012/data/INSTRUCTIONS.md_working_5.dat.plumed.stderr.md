Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[fv-az1429-301:04361] *** Process received signal ***
[fv-az1429-301:04361] Signal: Aborted (6)
[fv-az1429-301:04361] Signal code:  (-6)
[fv-az1429-301:04361] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6a71642520]
[fv-az1429-301:04361] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6a716969fc]
[fv-az1429-301:04361] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6a71642476]
[fv-az1429-301:04361] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6a716287f3]
[fv-az1429-301:04361] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6a71aa2b9e]
[fv-az1429-301:04361] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6a71aae20c]
[fv-az1429-301:04361] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6a71aae277]
[fv-az1429-301:04361] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6a71aae52b]
[fv-az1429-301:04361] [ 8] plumed(+0x12f48)[0x55b94a157f48]
[fv-az1429-301:04361] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6a71629d90]
[fv-az1429-301:04361] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6a71629e40]
[fv-az1429-301:04361] [11] plumed(+0x131e5)[0x55b94a1581e5]
[fv-az1429-301:04361] *** End of error message ***
</pre>
{% endraw %}
