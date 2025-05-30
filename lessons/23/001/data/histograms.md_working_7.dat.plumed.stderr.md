Stderr for source:  histograms.md_working_7.dat   
Download: [zipped raw stdout](histograms.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PAIRENTROPY LABEL=pp GROUP=1-108 MAXR=2.0 GRID_BIN=20 CUTOFF=1.5 BANDWIDTH=0.13
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61261] *** Process received signal ***
[pkrvmf6wy0o8zjz:61261] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61261] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61261] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4650c45330]
[pkrvmf6wy0o8zjz:61261] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4650c9eb2c]
[pkrvmf6wy0o8zjz:61261] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4650c4527e]
[pkrvmf6wy0o8zjz:61261] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4650c288ff]
[pkrvmf6wy0o8zjz:61261] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f46510a5ff5]
[pkrvmf6wy0o8zjz:61261] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f46510bb0da]
[pkrvmf6wy0o8zjz:61261] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f46510a5a55]
[pkrvmf6wy0o8zjz:61261] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f46510a5a6f]
[pkrvmf6wy0o8zjz:61261] [ 8] plumed(+0x13209)[0x55c6ab969209]
[pkrvmf6wy0o8zjz:61261] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4650c2a1ca]
[pkrvmf6wy0o8zjz:61261] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4650c2a28b]
[pkrvmf6wy0o8zjz:61261] [11] plumed(+0x134a5)[0x55c6ab9694a5]
[pkrvmf6wy0o8zjz:61261] *** End of error message ***
</pre>
{% endraw %}
