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
[pkrvmf6wy0o8zjz:61368] *** Process received signal ***
[pkrvmf6wy0o8zjz:61368] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61368] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61368] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f90b4445330]
[pkrvmf6wy0o8zjz:61368] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f90b449eb2c]
[pkrvmf6wy0o8zjz:61368] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f90b444527e]
[pkrvmf6wy0o8zjz:61368] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f90b44288ff]
[pkrvmf6wy0o8zjz:61368] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f90b48a5ff5]
[pkrvmf6wy0o8zjz:61368] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f90b48bb0da]
[pkrvmf6wy0o8zjz:61368] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f90b48a5a55]
[pkrvmf6wy0o8zjz:61368] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f90b48a5a6f]
[pkrvmf6wy0o8zjz:61368] [ 8] plumed(+0x13209)[0x55e58c7c5209]
[pkrvmf6wy0o8zjz:61368] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f90b442a1ca]
[pkrvmf6wy0o8zjz:61368] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f90b442a28b]
[pkrvmf6wy0o8zjz:61368] [11] plumed(+0x134a5)[0x55e58c7c54a5]
[pkrvmf6wy0o8zjz:61368] *** End of error message ***
</pre>
{% endraw %}
