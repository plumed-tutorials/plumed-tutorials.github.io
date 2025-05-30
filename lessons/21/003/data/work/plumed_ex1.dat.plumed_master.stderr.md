Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @34 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:60378] *** Process received signal ***
[pkrvmf6wy0o8zjz:60378] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60378] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60378] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f37e4045330]
[pkrvmf6wy0o8zjz:60378] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f37e409eb2c]
[pkrvmf6wy0o8zjz:60378] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f37e404527e]
[pkrvmf6wy0o8zjz:60378] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f37e40288ff]
[pkrvmf6wy0o8zjz:60378] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f37e44a5ff5]
[pkrvmf6wy0o8zjz:60378] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f37e44bb0da]
[pkrvmf6wy0o8zjz:60378] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f37e44a5a55]
[pkrvmf6wy0o8zjz:60378] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f37e44a5a6f]
[pkrvmf6wy0o8zjz:60378] [ 8] plumed_master(+0x146dd)[0x5626858a76dd]
[pkrvmf6wy0o8zjz:60378] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f37e402a1ca]
[pkrvmf6wy0o8zjz:60378] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f37e402a28b]
[pkrvmf6wy0o8zjz:60378] [11] plumed_master(+0x15365)[0x5626858a8365]
[pkrvmf6wy0o8zjz:60378] *** End of error message ***
</pre>
{% endraw %}
