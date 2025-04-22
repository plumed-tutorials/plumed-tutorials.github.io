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
[fv-az1315-757:07893] *** Process received signal ***
[fv-az1315-757:07893] Signal: Aborted (6)
[fv-az1315-757:07893] Signal code:  (-6)
[fv-az1315-757:07893] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5a2d245330]
[fv-az1315-757:07893] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5a2d29eb2c]
[fv-az1315-757:07893] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5a2d24527e]
[fv-az1315-757:07893] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5a2d2288ff]
[fv-az1315-757:07893] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5a2d6a5ff5]
[fv-az1315-757:07893] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5a2d6bb0da]
[fv-az1315-757:07893] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5a2d6a5a55]
[fv-az1315-757:07893] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5a2d6a5a6f]
[fv-az1315-757:07893] [ 8] plumed(+0x13209)[0x5582b3876209]
[fv-az1315-757:07893] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5a2d22a1ca]
[fv-az1315-757:07893] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5a2d22a28b]
[fv-az1315-757:07893] [11] plumed(+0x134a5)[0x5582b38764a5]
[fv-az1315-757:07893] *** End of error message ***
</pre>
{% endraw %}
