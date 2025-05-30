Stderr for source:  RMSD.md_working_1.dat   
Download: [zipped raw stdout](RMSD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONSTANT with label v : cannot understand the following words from the input line : NCOLS=12, NROWS=2
[pkrvmf6wy0o8zjz:61616] *** Process received signal ***
[pkrvmf6wy0o8zjz:61616] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61616] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61616] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5806045330]
[pkrvmf6wy0o8zjz:61616] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f580609eb2c]
[pkrvmf6wy0o8zjz:61616] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f580604527e]
[pkrvmf6wy0o8zjz:61616] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f58060288ff]
[pkrvmf6wy0o8zjz:61616] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f58064a5ff5]
[pkrvmf6wy0o8zjz:61616] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f58064bb0da]
[pkrvmf6wy0o8zjz:61616] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f58064a5a55]
[pkrvmf6wy0o8zjz:61616] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f58064a5a6f]
[pkrvmf6wy0o8zjz:61616] [ 8] plumed(+0x13209)[0x55a39d912209]
[pkrvmf6wy0o8zjz:61616] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f580602a1ca]
[pkrvmf6wy0o8zjz:61616] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f580602a28b]
[pkrvmf6wy0o8zjz:61616] [11] plumed(+0x134a5)[0x55a39d9124a5]
[pkrvmf6wy0o8zjz:61616] *** End of error message ***
</pre>
{% endraw %}
