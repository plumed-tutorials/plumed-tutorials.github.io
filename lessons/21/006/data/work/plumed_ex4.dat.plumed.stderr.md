Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DUMPPDB ATOMS=cc_data ATOM_INDICES=@nonhydrogens FILE=traj.pdb
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60062] *** Process received signal ***
[pkrvmf6wy0o8zjz:60062] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60062] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60062] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0898845330]
[pkrvmf6wy0o8zjz:60062] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f089889eb2c]
[pkrvmf6wy0o8zjz:60062] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f089884527e]
[pkrvmf6wy0o8zjz:60062] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f08988288ff]
[pkrvmf6wy0o8zjz:60062] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0898ca5ff5]
[pkrvmf6wy0o8zjz:60062] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0898cbb0da]
[pkrvmf6wy0o8zjz:60062] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0898ca5a55]
[pkrvmf6wy0o8zjz:60062] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0898ca5a6f]
[pkrvmf6wy0o8zjz:60062] [ 8] plumed(+0x13209)[0x55efc3c77209]
[pkrvmf6wy0o8zjz:60062] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f089882a1ca]
[pkrvmf6wy0o8zjz:60062] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f089882a28b]
[pkrvmf6wy0o8zjz:60062] [11] plumed(+0x134a5)[0x55efc3c774a5]
[pkrvmf6wy0o8zjz:60062] *** End of error message ***
</pre>
{% endraw %}
