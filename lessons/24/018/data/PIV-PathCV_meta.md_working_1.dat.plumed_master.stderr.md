Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1690-151:05657] *** Process received signal ***
[fv-az1690-151:05657] Signal: Aborted (6)
[fv-az1690-151:05657] Signal code:  (-6)
[fv-az1690-151:05657] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9565045330]
[fv-az1690-151:05657] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f956509eb2c]
[fv-az1690-151:05657] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f956504527e]
[fv-az1690-151:05657] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f95650288ff]
[fv-az1690-151:05657] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f95654a5ff5]
[fv-az1690-151:05657] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f95654bb0da]
[fv-az1690-151:05657] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f95654a5a55]
[fv-az1690-151:05657] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f95654a5a6f]
[fv-az1690-151:05657] [ 8] plumed_master(+0x146dd)[0x55ba5db1f6dd]
[fv-az1690-151:05657] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f956502a1ca]
[fv-az1690-151:05657] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f956502a28b]
[fv-az1690-151:05657] [11] plumed_master(+0x15365)[0x55ba5db20365]
[fv-az1690-151:05657] *** End of error message ***
</pre>
{% endraw %}
