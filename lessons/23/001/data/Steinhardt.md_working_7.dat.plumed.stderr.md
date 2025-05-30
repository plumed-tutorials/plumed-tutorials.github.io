Stderr for source:  Steinhardt.md_working_7.dat   
Download: [zipped raw stdout](Steinhardt.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 MEAN
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:59844] *** Process received signal ***
[pkrvmf6wy0o8zjz:59844] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59844] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59844] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3cd1845330]
[pkrvmf6wy0o8zjz:59844] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3cd189eb2c]
[pkrvmf6wy0o8zjz:59844] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3cd184527e]
[pkrvmf6wy0o8zjz:59844] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3cd18288ff]
[pkrvmf6wy0o8zjz:59844] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3cd1ca5ff5]
[pkrvmf6wy0o8zjz:59844] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3cd1cbb0da]
[pkrvmf6wy0o8zjz:59844] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3cd1ca5a55]
[pkrvmf6wy0o8zjz:59844] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3cd1ca5a6f]
[pkrvmf6wy0o8zjz:59844] [ 8] plumed(+0x13209)[0x562cf48f0209]
[pkrvmf6wy0o8zjz:59844] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3cd182a1ca]
[pkrvmf6wy0o8zjz:59844] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3cd182a28b]
[pkrvmf6wy0o8zjz:59844] [11] plumed(+0x134a5)[0x562cf48f04a5]
[pkrvmf6wy0o8zjz:59844] *** End of error message ***
</pre>
{% endraw %}
