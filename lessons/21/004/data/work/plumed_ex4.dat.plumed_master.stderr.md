Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @65 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:60622] *** Process received signal ***
[pkrvmf6wy0o8zjz:60622] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60622] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60622] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f953e445330]
[pkrvmf6wy0o8zjz:60622] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f953e49eb2c]
[pkrvmf6wy0o8zjz:60622] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f953e44527e]
[pkrvmf6wy0o8zjz:60622] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f953e4288ff]
[pkrvmf6wy0o8zjz:60622] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f953e8a5ff5]
[pkrvmf6wy0o8zjz:60622] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f953e8bb0da]
[pkrvmf6wy0o8zjz:60622] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f953e8a5a55]
[pkrvmf6wy0o8zjz:60622] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f953e8a5a6f]
[pkrvmf6wy0o8zjz:60622] [ 8] plumed_master(+0x146dd)[0x55d64f5ce6dd]
[pkrvmf6wy0o8zjz:60622] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f953e42a1ca]
[pkrvmf6wy0o8zjz:60622] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f953e42a28b]
[pkrvmf6wy0o8zjz:60622] [11] plumed_master(+0x15365)[0x55d64f5cf365]
[pkrvmf6wy0o8zjz:60622] *** End of error message ***
</pre>
{% endraw %}
