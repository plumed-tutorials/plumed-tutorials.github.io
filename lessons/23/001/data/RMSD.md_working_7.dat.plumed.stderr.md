Stderr for source:  RMSD.md_working_7.dat   
Download: [zipped raw stdout](RMSD.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PDB2CONSTANT LABEL=rmsd_ref REFERENCE=reference.pdb
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61792] *** Process received signal ***
[pkrvmf6wy0o8zjz:61792] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61792] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61792] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc0b1245330]
[pkrvmf6wy0o8zjz:61792] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc0b129eb2c]
[pkrvmf6wy0o8zjz:61792] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc0b124527e]
[pkrvmf6wy0o8zjz:61792] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc0b12288ff]
[pkrvmf6wy0o8zjz:61792] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc0b16a5ff5]
[pkrvmf6wy0o8zjz:61792] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc0b16bb0da]
[pkrvmf6wy0o8zjz:61792] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc0b16a5a55]
[pkrvmf6wy0o8zjz:61792] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc0b16a5a6f]
[pkrvmf6wy0o8zjz:61792] [ 8] plumed(+0x13209)[0x55f31f13d209]
[pkrvmf6wy0o8zjz:61792] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc0b122a1ca]
[pkrvmf6wy0o8zjz:61792] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc0b122a28b]
[pkrvmf6wy0o8zjz:61792] [11] plumed(+0x134a5)[0x55f31f13d4a5]
[pkrvmf6wy0o8zjz:61792] *** End of error message ***
</pre>
{% endraw %}
