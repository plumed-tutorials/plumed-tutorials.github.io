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
[pkrvmf6wy0o8zjz:58902] *** Process received signal ***
[pkrvmf6wy0o8zjz:58902] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58902] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58902] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb843245330]
[pkrvmf6wy0o8zjz:58902] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb84329eb2c]
[pkrvmf6wy0o8zjz:58902] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb84324527e]
[pkrvmf6wy0o8zjz:58902] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb8432288ff]
[pkrvmf6wy0o8zjz:58902] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb8436a5ff5]
[pkrvmf6wy0o8zjz:58902] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb8436bb0da]
[pkrvmf6wy0o8zjz:58902] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb8436a5a55]
[pkrvmf6wy0o8zjz:58902] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb8436a5a6f]
[pkrvmf6wy0o8zjz:58902] [ 8] plumed_master(+0x146dd)[0x55c50d53d6dd]
[pkrvmf6wy0o8zjz:58902] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb84322a1ca]
[pkrvmf6wy0o8zjz:58902] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb84322a28b]
[pkrvmf6wy0o8zjz:58902] [11] plumed_master(+0x15365)[0x55c50d53e365]
[pkrvmf6wy0o8zjz:58902] *** End of error message ***
</pre>
{% endraw %}
