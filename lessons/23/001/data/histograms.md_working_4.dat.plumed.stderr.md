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
[pkrvmf6wy0o8zjz:60915] *** Process received signal ***
[pkrvmf6wy0o8zjz:60915] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60915] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60915] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f68f0645330]
[pkrvmf6wy0o8zjz:60915] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f68f069eb2c]
[pkrvmf6wy0o8zjz:60915] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f68f064527e]
[pkrvmf6wy0o8zjz:60915] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f68f06288ff]
[pkrvmf6wy0o8zjz:60915] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f68f0aa5ff5]
[pkrvmf6wy0o8zjz:60915] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f68f0abb0da]
[pkrvmf6wy0o8zjz:60915] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f68f0aa5a55]
[pkrvmf6wy0o8zjz:60915] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f68f0aa5a6f]
[pkrvmf6wy0o8zjz:60915] [ 8] plumed(+0x13209)[0x564440ed8209]
[pkrvmf6wy0o8zjz:60915] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f68f062a1ca]
[pkrvmf6wy0o8zjz:60915] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f68f062a28b]
[pkrvmf6wy0o8zjz:60915] [11] plumed(+0x134a5)[0x564440ed84a5]
[pkrvmf6wy0o8zjz:60915] *** End of error message ***
</pre>
{% endraw %}
