Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label @s109 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver q6_mat q6_sh q6_denom_ones q6_denom q6_sp q6_rmn-n6 q6_imn-n6 q6_rmn-n5 q6_imn-n5 q6_rmn-n4 q6_imn-n4 q6_rmn-n3 q6_imn-n3 q6_rmn-n2 q6_imn-n2 q6_rmn-n1 q6_imn-n1 q6_rmn-0 q6_imn-0 q6_rmn-p1 q6_imn-p1 q6_rmn-p2 q6_imn-p2 q6_rmn-p3 q6_imn-p3 q6_rmn-p4 q6_imn-p4 q6_rmn-p5 q6_imn-p5 q6_rmn-p6 q6_imn-p6 q6_rms-n6 q6_ims-n6 q6_rms-n5 q6_ims-n5 q6_rms-n4 q6_ims-n4 q6_rms-n3 q6_ims-n3 q6_rms-n2 q6_ims-n2 q6_rms-n1 q6_ims-n1 q6_rms-0 q6_ims-0 q6_rms-p1 q6_ims-p1 q6_rms-p2 q6_ims-p2 q6_rms-p3 q6_ims-p3 q6_rms-p4 q6_ims-p4 q6_rms-p5 q6_ims-p5 q6_rms-p6 q6_ims-p6 q6_vmean2 q6_vmean q6_norm2 q6_norm q6 )
[pkrvmf6wy0o8zjz:59749] *** Process received signal ***
[pkrvmf6wy0o8zjz:59749] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59749] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59749] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6a00845330]
[pkrvmf6wy0o8zjz:59749] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6a0089eb2c]
[pkrvmf6wy0o8zjz:59749] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6a0084527e]
[pkrvmf6wy0o8zjz:59749] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6a008288ff]
[pkrvmf6wy0o8zjz:59749] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6a00ca5ff5]
[pkrvmf6wy0o8zjz:59749] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6a00cbb0da]
[pkrvmf6wy0o8zjz:59749] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6a00ca5a55]
[pkrvmf6wy0o8zjz:59749] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6a00ca5a6f]
[pkrvmf6wy0o8zjz:59749] [ 8] plumed_master(+0x146dd)[0x564818c696dd]
[pkrvmf6wy0o8zjz:59749] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6a0082a1ca]
[pkrvmf6wy0o8zjz:59749] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6a0082a28b]
[pkrvmf6wy0o8zjz:59749] [11] plumed_master(+0x15365)[0x564818c6a365]
[pkrvmf6wy0o8zjz:59749] *** End of error message ***
</pre>
{% endraw %}
