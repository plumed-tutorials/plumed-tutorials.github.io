Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label @s133 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver q6_mat q6_sh q6_denom_ones q6_denom q6_sp q6_rmn-n6 q6_imn-n6 q6_rmn-n5 q6_imn-n5 q6_rmn-n4 q6_imn-n4 q6_rmn-n3 q6_imn-n3 q6_rmn-n2 q6_imn-n2 q6_rmn-n1 q6_imn-n1 q6_rmn-0 q6_imn-0 q6_rmn-p1 q6_imn-p1 q6_rmn-p2 q6_imn-p2 q6_rmn-p3 q6_imn-p3 q6_rmn-p4 q6_imn-p4 q6_rmn-p5 q6_imn-p5 q6_rmn-p6 q6_imn-p6 q6_rms-n6 q6_ims-n6 q6_rms-n5 q6_ims-n5 q6_rms-n4 q6_ims-n4 q6_rms-n3 q6_ims-n3 q6_rms-n2 q6_ims-n2 q6_rms-n1 q6_ims-n1 q6_rms-0 q6_ims-0 q6_rms-p1 q6_ims-p1 q6_rms-p2 q6_ims-p2 q6_rms-p3 q6_ims-p3 q6_rms-p4 q6_ims-p4 q6_rms-p5 q6_ims-p5 q6_rms-p6 q6_ims-p6 q6_vmean2 q6_vmean q6_norm2 q6_norm q6 )
[fv-az2211-783:06171] *** Process received signal ***
[fv-az2211-783:06171] Signal: Aborted (6)
[fv-az2211-783:06171] Signal code:  (-6)
[fv-az2211-783:06171] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f850ba45330]
[fv-az2211-783:06171] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f850ba9eb2c]
[fv-az2211-783:06171] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f850ba4527e]
[fv-az2211-783:06171] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f850ba288ff]
[fv-az2211-783:06171] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f850bea5ff5]
[fv-az2211-783:06171] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f850bebb0da]
[fv-az2211-783:06171] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f850bea5a55]
[fv-az2211-783:06171] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f850bea5a6f]
[fv-az2211-783:06171] [ 8] plumed_master(+0x146dd)[0x5587f24826dd]
[fv-az2211-783:06171] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f850ba2a1ca]
[fv-az2211-783:06171] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f850ba2a28b]
[fv-az2211-783:06171] [11] plumed_master(+0x15365)[0x5587f2483365]
[fv-az2211-783:06171] *** End of error message ***
</pre>
{% endraw %}
