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
[pkrvmf6wy0o8zjz:61543] *** Process received signal ***
[pkrvmf6wy0o8zjz:61543] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61543] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61543] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd1a9645330]
[pkrvmf6wy0o8zjz:61543] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd1a969eb2c]
[pkrvmf6wy0o8zjz:61543] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd1a964527e]
[pkrvmf6wy0o8zjz:61543] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd1a96288ff]
[pkrvmf6wy0o8zjz:61543] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd1a9aa5ff5]
[pkrvmf6wy0o8zjz:61543] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd1a9abb0da]
[pkrvmf6wy0o8zjz:61543] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd1a9aa5a55]
[pkrvmf6wy0o8zjz:61543] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd1a9aa5a6f]
[pkrvmf6wy0o8zjz:61543] [ 8] plumed(+0x13209)[0x55a19f3ed209]
[pkrvmf6wy0o8zjz:61543] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd1a962a1ca]
[pkrvmf6wy0o8zjz:61543] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd1a962a28b]
[pkrvmf6wy0o8zjz:61543] [11] plumed(+0x134a5)[0x55a19f3ed4a5]
[pkrvmf6wy0o8zjz:61543] *** End of error message ***
</pre>
{% endraw %}
