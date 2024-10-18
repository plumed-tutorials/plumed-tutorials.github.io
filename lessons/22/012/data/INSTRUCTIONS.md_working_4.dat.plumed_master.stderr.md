Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1530-405:69703] *** Process received signal ***
[fv-az1530-405:69703] Signal: Aborted (6)
[fv-az1530-405:69703] Signal code:  (-6)
[fv-az1530-405:69703] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0880642520]
[fv-az1530-405:69703] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f08806969fc]
[fv-az1530-405:69703] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0880642476]
[fv-az1530-405:69703] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f08806287f3]
[fv-az1530-405:69703] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f0880aa2b9e]
[fv-az1530-405:69703] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f0880aae20c]
[fv-az1530-405:69703] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f0880aae277]
[fv-az1530-405:69703] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f0880aae52b]
[fv-az1530-405:69703] [ 8] plumed_master(+0x14254)[0x55ba07ac1254]
[fv-az1530-405:69703] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0880629d90]
[fv-az1530-405:69703] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0880629e40]
[fv-az1530-405:69703] [11] plumed_master(+0x14eb5)[0x55ba07ac1eb5]
[fv-az1530-405:69703] *** End of error message ***
</pre>
{% endraw %}
