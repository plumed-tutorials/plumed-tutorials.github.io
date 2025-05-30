Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label uwall : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:59777] *** Process received signal ***
[pkrvmf6wy0o8zjz:59777] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59777] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59777] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0889845330]
[pkrvmf6wy0o8zjz:59777] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f088989eb2c]
[pkrvmf6wy0o8zjz:59777] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f088984527e]
[pkrvmf6wy0o8zjz:59777] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f08898288ff]
[pkrvmf6wy0o8zjz:59777] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0889ca5ff5]
[pkrvmf6wy0o8zjz:59777] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0889cbb0da]
[pkrvmf6wy0o8zjz:59777] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0889ca5a55]
[pkrvmf6wy0o8zjz:59777] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0889ca5a6f]
[pkrvmf6wy0o8zjz:59777] [ 8] plumed(+0x13209)[0x555af7a56209]
[pkrvmf6wy0o8zjz:59777] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f088982a1ca]
[pkrvmf6wy0o8zjz:59777] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f088982a28b]
[pkrvmf6wy0o8zjz:59777] [11] plumed(+0x134a5)[0x555af7a564a5]
[pkrvmf6wy0o8zjz:59777] *** End of error message ***
</pre>
{% endraw %}
