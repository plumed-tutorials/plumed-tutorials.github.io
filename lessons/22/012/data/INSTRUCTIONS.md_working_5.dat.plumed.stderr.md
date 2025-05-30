Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[pkrvmf6wy0o8zjz:59733] *** Process received signal ***
[pkrvmf6wy0o8zjz:59733] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59733] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59733] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f110c045330]
[pkrvmf6wy0o8zjz:59733] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f110c09eb2c]
[pkrvmf6wy0o8zjz:59733] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f110c04527e]
[pkrvmf6wy0o8zjz:59733] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f110c0288ff]
[pkrvmf6wy0o8zjz:59733] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f110c4a5ff5]
[pkrvmf6wy0o8zjz:59733] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f110c4bb0da]
[pkrvmf6wy0o8zjz:59733] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f110c4a5a55]
[pkrvmf6wy0o8zjz:59733] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f110c4a5a6f]
[pkrvmf6wy0o8zjz:59733] [ 8] plumed(+0x13209)[0x55913b1d2209]
[pkrvmf6wy0o8zjz:59733] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f110c02a1ca]
[pkrvmf6wy0o8zjz:59733] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f110c02a28b]
[pkrvmf6wy0o8zjz:59733] [11] plumed(+0x134a5)[0x55913b1d24a5]
[pkrvmf6wy0o8zjz:59733] *** End of error message ***
</pre>
{% endraw %}
