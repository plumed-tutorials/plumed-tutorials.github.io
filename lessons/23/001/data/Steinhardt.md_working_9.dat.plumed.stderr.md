Stderr for source:  Steinhardt.md_working_9.dat   
Download: [zipped raw stdout](Steinhardt.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 VMEAN
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:59657] *** Process received signal ***
[pkrvmf6wy0o8zjz:59657] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59657] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59657] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb3c6845330]
[pkrvmf6wy0o8zjz:59657] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb3c689eb2c]
[pkrvmf6wy0o8zjz:59657] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb3c684527e]
[pkrvmf6wy0o8zjz:59657] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb3c68288ff]
[pkrvmf6wy0o8zjz:59657] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb3c6ca5ff5]
[pkrvmf6wy0o8zjz:59657] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb3c6cbb0da]
[pkrvmf6wy0o8zjz:59657] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb3c6ca5a55]
[pkrvmf6wy0o8zjz:59657] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb3c6ca5a6f]
[pkrvmf6wy0o8zjz:59657] [ 8] plumed(+0x13209)[0x560a872ba209]
[pkrvmf6wy0o8zjz:59657] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb3c682a1ca]
[pkrvmf6wy0o8zjz:59657] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb3c682a28b]
[pkrvmf6wy0o8zjz:59657] [11] plumed(+0x134a5)[0x560a872ba4a5]
[pkrvmf6wy0o8zjz:59657] *** End of error message ***
</pre>
{% endraw %}
