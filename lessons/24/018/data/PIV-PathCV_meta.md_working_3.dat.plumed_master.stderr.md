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
[runnervm3jyl0:79200] *** Process received signal ***
[runnervm3jyl0:79200] Signal: Aborted (6)
[runnervm3jyl0:79200] Signal code:  (-6)
[runnervm3jyl0:79200] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f35b3445330]
[runnervm3jyl0:79200] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f35b349eb2c]
[runnervm3jyl0:79200] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f35b344527e]
[runnervm3jyl0:79200] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f35b34288ff]
[runnervm3jyl0:79200] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f35b38a5ff5]
[runnervm3jyl0:79200] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f35b38bb0da]
[runnervm3jyl0:79200] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f35b38a5a55]
[runnervm3jyl0:79200] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f35b38a5a6f]
[runnervm3jyl0:79200] [ 8] plumed_master(+0x146dd)[0x55a83319b6dd]
[runnervm3jyl0:79200] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f35b342a1ca]
[runnervm3jyl0:79200] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f35b342a28b]
[runnervm3jyl0:79200] [11] plumed_master(+0x15365)[0x55a83319c365]
[runnervm3jyl0:79200] *** End of error message ***
</pre>
{% endraw %}
