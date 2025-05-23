Stderr for source:  histograms.md_working_3.dat   
Download: [zipped raw stdout](histograms.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 HEIGHTS=hA_h METRIC=hA_icov
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60884] *** Process received signal ***
[pkrvmf6wy0o8zjz:60884] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60884] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60884] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa126445330]
[pkrvmf6wy0o8zjz:60884] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa12649eb2c]
[pkrvmf6wy0o8zjz:60884] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa12644527e]
[pkrvmf6wy0o8zjz:60884] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa1264288ff]
[pkrvmf6wy0o8zjz:60884] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa1268a5ff5]
[pkrvmf6wy0o8zjz:60884] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa1268bb0da]
[pkrvmf6wy0o8zjz:60884] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa1268a5a55]
[pkrvmf6wy0o8zjz:60884] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa1268a5a6f]
[pkrvmf6wy0o8zjz:60884] [ 8] plumed(+0x13209)[0x559684c9d209]
[pkrvmf6wy0o8zjz:60884] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa12642a1ca]
[pkrvmf6wy0o8zjz:60884] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa12642a28b]
[pkrvmf6wy0o8zjz:60884] [11] plumed(+0x134a5)[0x559684c9d4a5]
[pkrvmf6wy0o8zjz:60884] *** End of error message ***
</pre>
{% endraw %}
