Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmf6wy0o8zjz:59778] *** Process received signal ***
[pkrvmf6wy0o8zjz:59778] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59778] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59778] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2868245330]
[pkrvmf6wy0o8zjz:59778] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f286829eb2c]
[pkrvmf6wy0o8zjz:59778] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f286824527e]
[pkrvmf6wy0o8zjz:59778] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f28682288ff]
[pkrvmf6wy0o8zjz:59778] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f28686a5ff5]
[pkrvmf6wy0o8zjz:59778] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f28686bb0da]
[pkrvmf6wy0o8zjz:59778] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f28686a5a55]
[pkrvmf6wy0o8zjz:59778] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f28686a5a6f]
[pkrvmf6wy0o8zjz:59778] [ 8] plumed_master(+0x146dd)[0x56539ddda6dd]
[pkrvmf6wy0o8zjz:59778] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f286822a1ca]
[pkrvmf6wy0o8zjz:59778] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f286822a28b]
[pkrvmf6wy0o8zjz:59778] [11] plumed_master(+0x15365)[0x56539dddb365]
[pkrvmf6wy0o8zjz:59778] *** End of error message ***
</pre>
{% endraw %}
