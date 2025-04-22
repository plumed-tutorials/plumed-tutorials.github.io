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
[fv-az2211-783:05762] *** Process received signal ***
[fv-az2211-783:05762] Signal: Aborted (6)
[fv-az2211-783:05762] Signal code:  (-6)
[fv-az2211-783:05762] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9077a45330]
[fv-az2211-783:05762] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9077a9eb2c]
[fv-az2211-783:05762] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9077a4527e]
[fv-az2211-783:05762] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9077a288ff]
[fv-az2211-783:05762] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9077ea5ff5]
[fv-az2211-783:05762] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9077ebb0da]
[fv-az2211-783:05762] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9077ea5a55]
[fv-az2211-783:05762] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9077ea5a6f]
[fv-az2211-783:05762] [ 8] plumed_master(+0x146dd)[0x5578207326dd]
[fv-az2211-783:05762] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9077a2a1ca]
[fv-az2211-783:05762] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9077a2a28b]
[fv-az2211-783:05762] [11] plumed_master(+0x15365)[0x557820733365]
[fv-az2211-783:05762] *** End of error message ***
</pre>
{% endraw %}
