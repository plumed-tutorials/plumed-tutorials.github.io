Stderr for source:  work/plumed_ex10.dat   
Download: [zipped raw stdout](plumed_ex10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60198] *** Process received signal ***
[pkrvmf6wy0o8zjz:60198] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60198] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60198] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5323445330]
[pkrvmf6wy0o8zjz:60198] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f532349eb2c]
[pkrvmf6wy0o8zjz:60198] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f532344527e]
[pkrvmf6wy0o8zjz:60198] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f53234288ff]
[pkrvmf6wy0o8zjz:60198] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f53238a5ff5]
[pkrvmf6wy0o8zjz:60198] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f53238bb0da]
[pkrvmf6wy0o8zjz:60198] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f53238a5a55]
[pkrvmf6wy0o8zjz:60198] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f53238a5a6f]
[pkrvmf6wy0o8zjz:60198] [ 8] plumed(+0x13209)[0x55859a17d209]
[pkrvmf6wy0o8zjz:60198] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f532342a1ca]
[pkrvmf6wy0o8zjz:60198] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f532342a28b]
[pkrvmf6wy0o8zjz:60198] [11] plumed(+0x134a5)[0x55859a17d4a5]
[pkrvmf6wy0o8zjz:60198] *** End of error message ***
</pre>
{% endraw %}
