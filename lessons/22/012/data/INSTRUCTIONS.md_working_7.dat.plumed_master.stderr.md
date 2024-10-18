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
[fv-az1530-405:69772] *** Process received signal ***
[fv-az1530-405:69772] Signal: Aborted (6)
[fv-az1530-405:69772] Signal code:  (-6)
[fv-az1530-405:69772] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4f87a42520]
[fv-az1530-405:69772] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4f87a969fc]
[fv-az1530-405:69772] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4f87a42476]
[fv-az1530-405:69772] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4f87a287f3]
[fv-az1530-405:69772] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4f87ea2b9e]
[fv-az1530-405:69772] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4f87eae20c]
[fv-az1530-405:69772] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4f87eae277]
[fv-az1530-405:69772] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4f87eae52b]
[fv-az1530-405:69772] [ 8] plumed_master(+0x14254)[0x563a723af254]
[fv-az1530-405:69772] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4f87a29d90]
[fv-az1530-405:69772] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4f87a29e40]
[fv-az1530-405:69772] [11] plumed_master(+0x14eb5)[0x563a723afeb5]
[fv-az1530-405:69772] *** End of error message ***
</pre>
{% endraw %}
