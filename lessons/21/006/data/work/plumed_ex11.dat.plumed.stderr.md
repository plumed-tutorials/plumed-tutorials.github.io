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
[pkrvmf6wy0o8zjz:60229] *** Process received signal ***
[pkrvmf6wy0o8zjz:60229] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60229] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60229] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f900f845330]
[pkrvmf6wy0o8zjz:60229] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f900f89eb2c]
[pkrvmf6wy0o8zjz:60229] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f900f84527e]
[pkrvmf6wy0o8zjz:60229] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f900f8288ff]
[pkrvmf6wy0o8zjz:60229] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f900fca5ff5]
[pkrvmf6wy0o8zjz:60229] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f900fcbb0da]
[pkrvmf6wy0o8zjz:60229] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f900fca5a55]
[pkrvmf6wy0o8zjz:60229] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f900fca5a6f]
[pkrvmf6wy0o8zjz:60229] [ 8] plumed(+0x13209)[0x5558afab3209]
[pkrvmf6wy0o8zjz:60229] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f900f82a1ca]
[pkrvmf6wy0o8zjz:60229] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f900f82a28b]
[pkrvmf6wy0o8zjz:60229] [11] plumed(+0x134a5)[0x5558afab34a5]
[pkrvmf6wy0o8zjz:60229] *** End of error message ***
</pre>
{% endraw %}
