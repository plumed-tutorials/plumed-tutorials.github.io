Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action UPPER_WALLS with label @s9 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1429-301:04393] *** Process received signal ***
[fv-az1429-301:04393] Signal: Aborted (6)
[fv-az1429-301:04393] Signal code:  (-6)
[fv-az1429-301:04393] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f735d042520]
[fv-az1429-301:04393] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f735d0969fc]
[fv-az1429-301:04393] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f735d042476]
[fv-az1429-301:04393] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f735d0287f3]
[fv-az1429-301:04393] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f735d4a2b9e]
[fv-az1429-301:04393] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f735d4ae20c]
[fv-az1429-301:04393] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f735d4ae277]
[fv-az1429-301:04393] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f735d4ae52b]
[fv-az1429-301:04393] [ 8] plumed_master(+0x14254)[0x557a1b50e254]
[fv-az1429-301:04393] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f735d029d90]
[fv-az1429-301:04393] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f735d029e40]
[fv-az1429-301:04393] [11] plumed_master(+0x14eb5)[0x557a1b50eeb5]
[fv-az1429-301:04393] *** End of error message ***
</pre>
{% endraw %}
