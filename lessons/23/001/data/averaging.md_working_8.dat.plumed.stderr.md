Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60703] *** Process received signal ***
[pkrvmf6wy0o8zjz:60703] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60703] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60703] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f800d645330]
[pkrvmf6wy0o8zjz:60703] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f800d69eb2c]
[pkrvmf6wy0o8zjz:60703] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f800d64527e]
[pkrvmf6wy0o8zjz:60703] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f800d6288ff]
[pkrvmf6wy0o8zjz:60703] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f800daa5ff5]
[pkrvmf6wy0o8zjz:60703] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f800dabb0da]
[pkrvmf6wy0o8zjz:60703] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f800daa5a55]
[pkrvmf6wy0o8zjz:60703] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f800daa5a6f]
[pkrvmf6wy0o8zjz:60703] [ 8] plumed(+0x13209)[0x55d7e7cd4209]
[pkrvmf6wy0o8zjz:60703] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f800d62a1ca]
[pkrvmf6wy0o8zjz:60703] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f800d62a28b]
[pkrvmf6wy0o8zjz:60703] [11] plumed(+0x134a5)[0x55d7e7cd44a5]
[pkrvmf6wy0o8zjz:60703] *** End of error message ***
</pre>
{% endraw %}
