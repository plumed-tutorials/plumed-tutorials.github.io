Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1429-301:04416] *** Process received signal ***
[fv-az1429-301:04416] Signal: Aborted (6)
[fv-az1429-301:04416] Signal code:  (-6)
[fv-az1429-301:04416] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa9fea42520]
[fv-az1429-301:04416] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa9fea969fc]
[fv-az1429-301:04416] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa9fea42476]
[fv-az1429-301:04416] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa9fea287f3]
[fv-az1429-301:04416] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa9feea2b9e]
[fv-az1429-301:04416] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa9feeae20c]
[fv-az1429-301:04416] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa9feeae277]
[fv-az1429-301:04416] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa9feeae52b]
[fv-az1429-301:04416] [ 8] plumed_master(+0x14254)[0x55ea0b917254]
[fv-az1429-301:04416] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa9fea29d90]
[fv-az1429-301:04416] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa9fea29e40]
[fv-az1429-301:04416] [11] plumed_master(+0x14eb5)[0x55ea0b917eb5]
[fv-az1429-301:04416] *** End of error message ***
</pre>
{% endraw %}
