Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:59039] *** Process received signal ***
[pkrvmf6wy0o8zjz:59039] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59039] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59039] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f868a245330]
[pkrvmf6wy0o8zjz:59039] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f868a29eb2c]
[pkrvmf6wy0o8zjz:59039] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f868a24527e]
[pkrvmf6wy0o8zjz:59039] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f868a2288ff]
[pkrvmf6wy0o8zjz:59039] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f868a6a5ff5]
[pkrvmf6wy0o8zjz:59039] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f868a6bb0da]
[pkrvmf6wy0o8zjz:59039] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f868a6a5a55]
[pkrvmf6wy0o8zjz:59039] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f868a6a5a6f]
[pkrvmf6wy0o8zjz:59039] [ 8] plumed(+0x13209)[0x55e258446209]
[pkrvmf6wy0o8zjz:59039] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f868a22a1ca]
[pkrvmf6wy0o8zjz:59039] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f868a22a28b]
[pkrvmf6wy0o8zjz:59039] [11] plumed(+0x134a5)[0x55e2584464a5]
[pkrvmf6wy0o8zjz:59039] *** End of error message ***
</pre>
{% endraw %}
