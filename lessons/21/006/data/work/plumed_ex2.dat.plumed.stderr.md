Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PCA with label pca : action cc has no component named cc (hint! the components in this actions are: )
[pkrvmf6wy0o8zjz:60297] *** Process received signal ***
[pkrvmf6wy0o8zjz:60297] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60297] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60297] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb730245330]
[pkrvmf6wy0o8zjz:60297] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb73029eb2c]
[pkrvmf6wy0o8zjz:60297] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb73024527e]
[pkrvmf6wy0o8zjz:60297] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb7302288ff]
[pkrvmf6wy0o8zjz:60297] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb7306a5ff5]
[pkrvmf6wy0o8zjz:60297] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb7306bb0da]
[pkrvmf6wy0o8zjz:60297] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb7306a5a55]
[pkrvmf6wy0o8zjz:60297] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb7306a5a6f]
[pkrvmf6wy0o8zjz:60297] [ 8] plumed(+0x13209)[0x557b05583209]
[pkrvmf6wy0o8zjz:60297] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb73022a1ca]
[pkrvmf6wy0o8zjz:60297] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb73022a28b]
[pkrvmf6wy0o8zjz:60297] [11] plumed(+0x134a5)[0x557b055834a5]
[pkrvmf6wy0o8zjz:60297] *** End of error message ***
</pre>
{% endraw %}
