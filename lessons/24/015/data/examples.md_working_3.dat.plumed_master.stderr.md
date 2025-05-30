Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:59013] *** Process received signal ***
[pkrvmf6wy0o8zjz:59013] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59013] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59013] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f27a5245330]
[pkrvmf6wy0o8zjz:59013] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f27a529eb2c]
[pkrvmf6wy0o8zjz:59013] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f27a524527e]
[pkrvmf6wy0o8zjz:59013] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f27a52288ff]
[pkrvmf6wy0o8zjz:59013] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f27a56a5ff5]
[pkrvmf6wy0o8zjz:59013] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f27a56bb0da]
[pkrvmf6wy0o8zjz:59013] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f27a56a5a55]
[pkrvmf6wy0o8zjz:59013] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f27a56a5a6f]
[pkrvmf6wy0o8zjz:59013] [ 8] plumed_master(+0x146dd)[0x5596bf7086dd]
[pkrvmf6wy0o8zjz:59013] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f27a522a1ca]
[pkrvmf6wy0o8zjz:59013] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f27a522a28b]
[pkrvmf6wy0o8zjz:59013] [11] plumed_master(+0x15365)[0x5596bf709365]
[pkrvmf6wy0o8zjz:59013] *** End of error message ***
</pre>
{% endraw %}
