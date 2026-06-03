Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[runnervm3jyl0:47284] *** Process received signal ***
[runnervm3jyl0:47284] Signal: Aborted (6)
[runnervm3jyl0:47284] Signal code:  (-6)
[runnervm3jyl0:47284] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2c9bc45330]
[runnervm3jyl0:47284] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2c9bc9eb2c]
[runnervm3jyl0:47284] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2c9bc4527e]
[runnervm3jyl0:47284] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2c9bc288ff]
[runnervm3jyl0:47284] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2c9c0a5ff5]
[runnervm3jyl0:47284] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2c9c0bb0da]
[runnervm3jyl0:47284] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2c9c0a5a55]
[runnervm3jyl0:47284] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2c9c0a5a6f]
[runnervm3jyl0:47284] [ 8] plumed_master(+0x146dd)[0x55f1e810a6dd]
[runnervm3jyl0:47284] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2c9bc2a1ca]
[runnervm3jyl0:47284] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2c9bc2a28b]
[runnervm3jyl0:47284] [11] plumed_master(+0x15365)[0x55f1e810b365]
[runnervm3jyl0:47284] *** End of error message ***
</pre>
{% endraw %}
