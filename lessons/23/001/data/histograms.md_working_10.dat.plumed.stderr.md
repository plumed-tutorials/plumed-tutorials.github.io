Stderr for source:  histograms.md_working_10.dat   
Download: [zipped raw stdout](histograms.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1
Maybe a missing space or a typo?
[fv-az1755-505:08007] *** Process received signal ***
[fv-az1755-505:08007] Signal: Aborted (6)
[fv-az1755-505:08007] Signal code:  (-6)
[fv-az1755-505:08007] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbef2445330]
[fv-az1755-505:08007] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbef249eb2c]
[fv-az1755-505:08007] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbef244527e]
[fv-az1755-505:08007] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbef24288ff]
[fv-az1755-505:08007] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbef28a5ff5]
[fv-az1755-505:08007] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbef28bb0da]
[fv-az1755-505:08007] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbef28a5a55]
[fv-az1755-505:08007] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbef28a5a6f]
[fv-az1755-505:08007] [ 8] plumed(+0x13209)[0x55d87c03c209]
[fv-az1755-505:08007] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbef242a1ca]
[fv-az1755-505:08007] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbef242a28b]
[fv-az1755-505:08007] [11] plumed(+0x134a5)[0x55d87c03c4a5]
[fv-az1755-505:08007] *** End of error message ***
</pre>
{% endraw %}
