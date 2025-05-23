Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:58823] *** Process received signal ***
[pkrvmf6wy0o8zjz:58823] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58823] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58823] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8215e45330]
[pkrvmf6wy0o8zjz:58823] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8215e9eb2c]
[pkrvmf6wy0o8zjz:58823] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8215e4527e]
[pkrvmf6wy0o8zjz:58823] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8215e288ff]
[pkrvmf6wy0o8zjz:58823] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f82162a5ff5]
[pkrvmf6wy0o8zjz:58823] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f82162bb0da]
[pkrvmf6wy0o8zjz:58823] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f82162a5a55]
[pkrvmf6wy0o8zjz:58823] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f82162a5a6f]
[pkrvmf6wy0o8zjz:58823] [ 8] plumed(+0x13209)[0x55b9c427d209]
[pkrvmf6wy0o8zjz:58823] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8215e2a1ca]
[pkrvmf6wy0o8zjz:58823] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8215e2a28b]
[pkrvmf6wy0o8zjz:58823] [11] plumed(+0x134a5)[0x55b9c427d4a5]
[pkrvmf6wy0o8zjz:58823] *** End of error message ***
</pre>
{% endraw %}
