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
[fv-az573-691:04452] *** Process received signal ***
[fv-az573-691:04452] Signal: Aborted (6)
[fv-az573-691:04452] Signal code:  (-6)
[fv-az573-691:04452] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc9b2a42520]
[fv-az573-691:04452] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc9b2a969fc]
[fv-az573-691:04452] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc9b2a42476]
[fv-az573-691:04452] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc9b2a287f3]
[fv-az573-691:04452] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc9b2ea2b9e]
[fv-az573-691:04452] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc9b2eae20c]
[fv-az573-691:04452] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc9b2eae277]
[fv-az573-691:04452] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc9b2eae52b]
[fv-az573-691:04452] [ 8] plumed(+0x12f48)[0x557133cfef48]
[fv-az573-691:04452] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc9b2a29d90]
[fv-az573-691:04452] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc9b2a29e40]
[fv-az573-691:04452] [11] plumed(+0x131e5)[0x557133cff1e5]
[fv-az573-691:04452] *** End of error message ***
</pre>
{% endraw %}
