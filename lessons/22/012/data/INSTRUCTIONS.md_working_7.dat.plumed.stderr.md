Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az1429-301:04408] *** Process received signal ***
[fv-az1429-301:04408] Signal: Aborted (6)
[fv-az1429-301:04408] Signal code:  (-6)
[fv-az1429-301:04408] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd585242520]
[fv-az1429-301:04408] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd5852969fc]
[fv-az1429-301:04408] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd585242476]
[fv-az1429-301:04408] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd5852287f3]
[fv-az1429-301:04408] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd5856a2b9e]
[fv-az1429-301:04408] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd5856ae20c]
[fv-az1429-301:04408] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd5856ae277]
[fv-az1429-301:04408] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd5856ae52b]
[fv-az1429-301:04408] [ 8] plumed(+0x12f48)[0x55f1a5c80f48]
[fv-az1429-301:04408] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd585229d90]
[fv-az1429-301:04408] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd585229e40]
[fv-az1429-301:04408] [11] plumed(+0x131e5)[0x55f1a5c811e5]
[fv-az1429-301:04408] *** End of error message ***
</pre>
{% endraw %}
