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
[fv-az573-691:04460] *** Process received signal ***
[fv-az573-691:04460] Signal: Aborted (6)
[fv-az573-691:04460] Signal code:  (-6)
[fv-az573-691:04460] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0244e42520]
[fv-az573-691:04460] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f0244e969fc]
[fv-az573-691:04460] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0244e42476]
[fv-az573-691:04460] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f0244e287f3]
[fv-az573-691:04460] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f02452a2b9e]
[fv-az573-691:04460] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f02452ae20c]
[fv-az573-691:04460] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f02452ae277]
[fv-az573-691:04460] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f02452ae52b]
[fv-az573-691:04460] [ 8] plumed_master(+0x14254)[0x55bf04eb2254]
[fv-az573-691:04460] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0244e29d90]
[fv-az573-691:04460] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0244e29e40]
[fv-az573-691:04460] [11] plumed_master(+0x14eb5)[0x55bf04eb2eb5]
[fv-az573-691:04460] *** End of error message ***
</pre>
{% endraw %}
