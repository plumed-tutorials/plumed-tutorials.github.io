Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[pkrvmf6wy0o8zjz:59626] *** Process received signal ***
[pkrvmf6wy0o8zjz:59626] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59626] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59626] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc070c45330]
[pkrvmf6wy0o8zjz:59626] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc070c9eb2c]
[pkrvmf6wy0o8zjz:59626] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc070c4527e]
[pkrvmf6wy0o8zjz:59626] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc070c288ff]
[pkrvmf6wy0o8zjz:59626] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc0710a5ff5]
[pkrvmf6wy0o8zjz:59626] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc0710bb0da]
[pkrvmf6wy0o8zjz:59626] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc0710a5a55]
[pkrvmf6wy0o8zjz:59626] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc0710a5a6f]
[pkrvmf6wy0o8zjz:59626] [ 8] plumed(+0x13209)[0x55d97ff59209]
[pkrvmf6wy0o8zjz:59626] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc070c2a1ca]
[pkrvmf6wy0o8zjz:59626] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc070c2a28b]
[pkrvmf6wy0o8zjz:59626] [11] plumed(+0x134a5)[0x55d97ff594a5]
[pkrvmf6wy0o8zjz:59626] *** End of error message ***
</pre>
{% endraw %}
