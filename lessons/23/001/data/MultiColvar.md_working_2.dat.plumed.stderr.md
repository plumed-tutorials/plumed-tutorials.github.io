Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:59041] *** Process received signal ***
[pkrvmf6wy0o8zjz:59041] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59041] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59041] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9f24245330]
[pkrvmf6wy0o8zjz:59041] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9f2429eb2c]
[pkrvmf6wy0o8zjz:59041] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9f2424527e]
[pkrvmf6wy0o8zjz:59041] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9f242288ff]
[pkrvmf6wy0o8zjz:59041] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9f246a5ff5]
[pkrvmf6wy0o8zjz:59041] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9f246bb0da]
[pkrvmf6wy0o8zjz:59041] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9f246a5a55]
[pkrvmf6wy0o8zjz:59041] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9f246a5a6f]
[pkrvmf6wy0o8zjz:59041] [ 8] plumed(+0x13209)[0x56145a215209]
[pkrvmf6wy0o8zjz:59041] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9f2422a1ca]
[pkrvmf6wy0o8zjz:59041] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9f2422a28b]
[pkrvmf6wy0o8zjz:59041] [11] plumed(+0x134a5)[0x56145a2154a5]
[pkrvmf6wy0o8zjz:59041] *** End of error message ***
</pre>
{% endraw %}
