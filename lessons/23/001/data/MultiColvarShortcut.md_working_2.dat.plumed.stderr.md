Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:59129] *** Process received signal ***
[pkrvmf6wy0o8zjz:59129] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59129] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59129] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3fe6045330]
[pkrvmf6wy0o8zjz:59129] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3fe609eb2c]
[pkrvmf6wy0o8zjz:59129] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3fe604527e]
[pkrvmf6wy0o8zjz:59129] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3fe60288ff]
[pkrvmf6wy0o8zjz:59129] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3fe64a5ff5]
[pkrvmf6wy0o8zjz:59129] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3fe64bb0da]
[pkrvmf6wy0o8zjz:59129] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3fe64a5a55]
[pkrvmf6wy0o8zjz:59129] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3fe64a5a6f]
[pkrvmf6wy0o8zjz:59129] [ 8] plumed(+0x13209)[0x56460abc4209]
[pkrvmf6wy0o8zjz:59129] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3fe602a1ca]
[pkrvmf6wy0o8zjz:59129] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3fe602a28b]
[pkrvmf6wy0o8zjz:59129] [11] plumed(+0x134a5)[0x56460abc44a5]
[pkrvmf6wy0o8zjz:59129] *** End of error message ***
</pre>
{% endraw %}
