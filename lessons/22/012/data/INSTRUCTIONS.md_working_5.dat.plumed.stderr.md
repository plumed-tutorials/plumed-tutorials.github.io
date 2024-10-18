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
[fv-az1530-405:69718] *** Process received signal ***
[fv-az1530-405:69718] Signal: Aborted (6)
[fv-az1530-405:69718] Signal code:  (-6)
[fv-az1530-405:69718] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff95d242520]
[fv-az1530-405:69718] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff95d2969fc]
[fv-az1530-405:69718] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff95d242476]
[fv-az1530-405:69718] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff95d2287f3]
[fv-az1530-405:69718] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff95d6a2b9e]
[fv-az1530-405:69718] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff95d6ae20c]
[fv-az1530-405:69718] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff95d6ae277]
[fv-az1530-405:69718] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff95d6ae52b]
[fv-az1530-405:69718] [ 8] plumed(+0x12f48)[0x558d683daf48]
[fv-az1530-405:69718] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff95d229d90]
[fv-az1530-405:69718] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff95d229e40]
[fv-az1530-405:69718] [11] plumed(+0x131e5)[0x558d683db1e5]
[fv-az1530-405:69718] *** End of error message ***
</pre>
{% endraw %}
