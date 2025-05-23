Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:59762] *** Process received signal ***
[pkrvmf6wy0o8zjz:59762] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59762] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59762] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7ff7e45330]
[pkrvmf6wy0o8zjz:59762] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7ff7e9eb2c]
[pkrvmf6wy0o8zjz:59762] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7ff7e4527e]
[pkrvmf6wy0o8zjz:59762] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7ff7e288ff]
[pkrvmf6wy0o8zjz:59762] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7ff82a5ff5]
[pkrvmf6wy0o8zjz:59762] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7ff82bb0da]
[pkrvmf6wy0o8zjz:59762] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7ff82a5a55]
[pkrvmf6wy0o8zjz:59762] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7ff82a5a6f]
[pkrvmf6wy0o8zjz:59762] [ 8] plumed(+0x13209)[0x561910ef6209]
[pkrvmf6wy0o8zjz:59762] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7ff7e2a1ca]
[pkrvmf6wy0o8zjz:59762] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7ff7e2a28b]
[pkrvmf6wy0o8zjz:59762] [11] plumed(+0x134a5)[0x561910ef64a5]
[pkrvmf6wy0o8zjz:59762] *** End of error message ***
</pre>
{% endraw %}
