Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label @s9 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmf6wy0o8zjz:59793] *** Process received signal ***
[pkrvmf6wy0o8zjz:59793] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59793] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59793] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe1f9245330]
[pkrvmf6wy0o8zjz:59793] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe1f929eb2c]
[pkrvmf6wy0o8zjz:59793] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe1f924527e]
[pkrvmf6wy0o8zjz:59793] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe1f92288ff]
[pkrvmf6wy0o8zjz:59793] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe1f96a5ff5]
[pkrvmf6wy0o8zjz:59793] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe1f96bb0da]
[pkrvmf6wy0o8zjz:59793] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe1f96a5a55]
[pkrvmf6wy0o8zjz:59793] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe1f96a5a6f]
[pkrvmf6wy0o8zjz:59793] [ 8] plumed_master(+0x146dd)[0x5589a74da6dd]
[pkrvmf6wy0o8zjz:59793] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe1f922a1ca]
[pkrvmf6wy0o8zjz:59793] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe1f922a28b]
[pkrvmf6wy0o8zjz:59793] [11] plumed_master(+0x15365)[0x5589a74db365]
[pkrvmf6wy0o8zjz:59793] *** End of error message ***
</pre>
{% endraw %}
