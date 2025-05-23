Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[pkrvmf6wy0o8zjz:59337] *** Process received signal ***
[pkrvmf6wy0o8zjz:59337] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59337] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59337] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb115a45330]
[pkrvmf6wy0o8zjz:59337] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb115a9eb2c]
[pkrvmf6wy0o8zjz:59337] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb115a4527e]
[pkrvmf6wy0o8zjz:59337] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb115a288ff]
[pkrvmf6wy0o8zjz:59337] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb115ea5ff5]
[pkrvmf6wy0o8zjz:59337] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb115ebb0da]
[pkrvmf6wy0o8zjz:59337] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb115ea5a55]
[pkrvmf6wy0o8zjz:59337] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb115ea5a6f]
[pkrvmf6wy0o8zjz:59337] [ 8] plumed(+0x13209)[0x563ab8b1c209]
[pkrvmf6wy0o8zjz:59337] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb115a2a1ca]
[pkrvmf6wy0o8zjz:59337] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb115a2a28b]
[pkrvmf6wy0o8zjz:59337] [11] plumed(+0x134a5)[0x563ab8b1c4a5]
[pkrvmf6wy0o8zjz:59337] *** End of error message ***
</pre>
{% endraw %}
