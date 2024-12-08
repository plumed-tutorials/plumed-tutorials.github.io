Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action MATHEVAL with label @s133 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver q6_mat q6_sh q6_denom_ones q6_denom q6_sp q6_rmn-n6 q6_imn-n6 q6_rmn-n5 q6_imn-n5 q6_rmn-n4 q6_imn-n4 q6_rmn-n3 q6_imn-n3 q6_rmn-n2 q6_imn-n2 q6_rmn-n1 q6_imn-n1 q6_rmn-0 q6_imn-0 q6_rmn-p1 q6_imn-p1 q6_rmn-p2 q6_imn-p2 q6_rmn-p3 q6_imn-p3 q6_rmn-p4 q6_imn-p4 q6_rmn-p5 q6_imn-p5 q6_rmn-p6 q6_imn-p6 q6_rms-n6 q6_ims-n6 q6_rms-n5 q6_ims-n5 q6_rms-n4 q6_ims-n4 q6_rms-n3 q6_ims-n3 q6_rms-n2 q6_ims-n2 q6_rms-n1 q6_ims-n1 q6_rms-0 q6_ims-0 q6_rms-p1 q6_ims-p1 q6_rms-p2 q6_ims-p2 q6_rms-p3 q6_ims-p3 q6_rms-p4 q6_ims-p4 q6_rms-p5 q6_ims-p5 q6_rms-p6 q6_ims-p6 q6_vmean2 q6_vmean q6_norm2 q6_norm q6 )
[fv-az1429-301:04369] *** Process received signal ***
[fv-az1429-301:04369] Signal: Aborted (6)
[fv-az1429-301:04369] Signal code:  (-6)
[fv-az1429-301:04369] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f7afde42520]
[fv-az1429-301:04369] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f7afde969fc]
[fv-az1429-301:04369] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f7afde42476]
[fv-az1429-301:04369] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f7afde287f3]
[fv-az1429-301:04369] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f7afe2a2b9e]
[fv-az1429-301:04369] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f7afe2ae20c]
[fv-az1429-301:04369] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f7afe2ae277]
[fv-az1429-301:04369] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f7afe2ae52b]
[fv-az1429-301:04369] [ 8] plumed_master(+0x14254)[0x55c099c83254]
[fv-az1429-301:04369] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f7afde29d90]
[fv-az1429-301:04369] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f7afde29e40]
[fv-az1429-301:04369] [11] plumed_master(+0x14eb5)[0x55c099c83eb5]
[fv-az1429-301:04369] *** End of error message ***
</pre>
{% endraw %}
