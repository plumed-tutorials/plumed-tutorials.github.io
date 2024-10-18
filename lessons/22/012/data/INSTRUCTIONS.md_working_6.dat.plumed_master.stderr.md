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
[fv-az1530-405:69749] *** Process received signal ***
[fv-az1530-405:69749] Signal: Aborted (6)
[fv-az1530-405:69749] Signal code:  (-6)
[fv-az1530-405:69749] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd7d2c42520]
[fv-az1530-405:69749] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd7d2c969fc]
[fv-az1530-405:69749] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd7d2c42476]
[fv-az1530-405:69749] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd7d2c287f3]
[fv-az1530-405:69749] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd7d30a2b9e]
[fv-az1530-405:69749] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd7d30ae20c]
[fv-az1530-405:69749] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd7d30ae277]
[fv-az1530-405:69749] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd7d30ae52b]
[fv-az1530-405:69749] [ 8] plumed_master(+0x14254)[0x55c5b5959254]
[fv-az1530-405:69749] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd7d2c29d90]
[fv-az1530-405:69749] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd7d2c29e40]
[fv-az1530-405:69749] [11] plumed_master(+0x14eb5)[0x55c5b5959eb5]
[fv-az1530-405:69749] *** End of error message ***
</pre>
{% endraw %}
