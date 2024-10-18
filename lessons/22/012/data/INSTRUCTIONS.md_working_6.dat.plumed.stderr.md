Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action UPPER_WALLS with label uwall : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az1530-405:69741] *** Process received signal ***
[fv-az1530-405:69741] Signal: Aborted (6)
[fv-az1530-405:69741] Signal code:  (-6)
[fv-az1530-405:69741] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f32f2842520]
[fv-az1530-405:69741] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f32f28969fc]
[fv-az1530-405:69741] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f32f2842476]
[fv-az1530-405:69741] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f32f28287f3]
[fv-az1530-405:69741] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f32f2ca2b9e]
[fv-az1530-405:69741] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f32f2cae20c]
[fv-az1530-405:69741] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f32f2cae277]
[fv-az1530-405:69741] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f32f2cae52b]
[fv-az1530-405:69741] [ 8] plumed(+0x12f48)[0x55ddcc902f48]
[fv-az1530-405:69741] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f32f2829d90]
[fv-az1530-405:69741] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f32f2829e40]
[fv-az1530-405:69741] [11] plumed(+0x131e5)[0x55ddcc9031e5]
[fv-az1530-405:69741] *** End of error message ***
</pre>
{% endraw %}
