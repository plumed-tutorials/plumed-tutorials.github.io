Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed.stderr.txt.zip) 
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
[pkrvmf6wy0o8zjz:60532] *** Process received signal ***
[pkrvmf6wy0o8zjz:60532] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60532] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60532] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2778845330]
[pkrvmf6wy0o8zjz:60532] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f277889eb2c]
[pkrvmf6wy0o8zjz:60532] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f277884527e]
[pkrvmf6wy0o8zjz:60532] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f27788288ff]
[pkrvmf6wy0o8zjz:60532] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2778ca5ff5]
[pkrvmf6wy0o8zjz:60532] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2778cbb0da]
[pkrvmf6wy0o8zjz:60532] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2778ca5a55]
[pkrvmf6wy0o8zjz:60532] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2778ca5a6f]
[pkrvmf6wy0o8zjz:60532] [ 8] plumed(+0x13209)[0x5571925dd209]
[pkrvmf6wy0o8zjz:60532] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f277882a1ca]
[pkrvmf6wy0o8zjz:60532] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f277882a28b]
[pkrvmf6wy0o8zjz:60532] [11] plumed(+0x134a5)[0x5571925dd4a5]
[pkrvmf6wy0o8zjz:60532] *** End of error message ***
</pre>
{% endraw %}
