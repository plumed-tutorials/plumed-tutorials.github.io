Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1778-96:04093] *** Process received signal ***
[fv-az1778-96:04093] Signal: Aborted (6)
[fv-az1778-96:04093] Signal code:  (-6)
[fv-az1778-96:04093] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f37bde42520]
[fv-az1778-96:04093] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f37bde969fc]
[fv-az1778-96:04093] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f37bde42476]
[fv-az1778-96:04093] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f37bde287f3]
[fv-az1778-96:04093] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f37be2a2b9e]
[fv-az1778-96:04093] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f37be2ae20c]
[fv-az1778-96:04093] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f37be2ae277]
[fv-az1778-96:04093] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f37be2ae52b]
[fv-az1778-96:04093] [ 8] plumed_master(+0x14254)[0x55c8de39b254]
[fv-az1778-96:04093] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f37bde29d90]
[fv-az1778-96:04093] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f37bde29e40]
[fv-az1778-96:04093] [11] plumed_master(+0x14eb5)[0x55c8de39beb5]
[fv-az1778-96:04093] *** End of error message ***
</pre>
{% endraw %}
