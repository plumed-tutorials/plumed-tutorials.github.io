Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1690-151:05721] *** Process received signal ***
[fv-az1690-151:05721] Signal: Aborted (6)
[fv-az1690-151:05721] Signal code:  (-6)
[fv-az1690-151:05721] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa01cc45330]
[fv-az1690-151:05721] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa01cc9eb2c]
[fv-az1690-151:05721] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa01cc4527e]
[fv-az1690-151:05721] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa01cc288ff]
[fv-az1690-151:05721] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa01d0a5ff5]
[fv-az1690-151:05721] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa01d0bb0da]
[fv-az1690-151:05721] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa01d0a5a55]
[fv-az1690-151:05721] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa01d0a5a6f]
[fv-az1690-151:05721] [ 8] plumed_master(+0x146dd)[0x5614a448a6dd]
[fv-az1690-151:05721] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa01cc2a1ca]
[fv-az1690-151:05721] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa01cc2a28b]
[fv-az1690-151:05721] [11] plumed_master(+0x15365)[0x5614a448b365]
[fv-az1690-151:05721] *** End of error message ***
</pre>
{% endraw %}
