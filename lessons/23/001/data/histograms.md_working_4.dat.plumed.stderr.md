Stderr for source:  histograms.md_working_4.dat   
Download: [zipped raw stdout](histograms.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=c1 GRID_MIN=0.0 GRID_MAX=12.0 GRID_BIN=120 BANDWIDTH=0.1
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61165] *** Process received signal ***
[pkrvmf6wy0o8zjz:61165] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61165] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61165] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc8a6645330]
[pkrvmf6wy0o8zjz:61165] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc8a669eb2c]
[pkrvmf6wy0o8zjz:61165] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc8a664527e]
[pkrvmf6wy0o8zjz:61165] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc8a66288ff]
[pkrvmf6wy0o8zjz:61165] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc8a6aa5ff5]
[pkrvmf6wy0o8zjz:61165] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc8a6abb0da]
[pkrvmf6wy0o8zjz:61165] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc8a6aa5a55]
[pkrvmf6wy0o8zjz:61165] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc8a6aa5a6f]
[pkrvmf6wy0o8zjz:61165] [ 8] plumed(+0x13209)[0x559439790209]
[pkrvmf6wy0o8zjz:61165] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc8a662a1ca]
[pkrvmf6wy0o8zjz:61165] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc8a662a28b]
[pkrvmf6wy0o8zjz:61165] [11] plumed(+0x134a5)[0x5594397904a5]
[pkrvmf6wy0o8zjz:61165] *** End of error message ***
</pre>
{% endraw %}
