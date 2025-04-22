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
[fv-az1315-757:07990] *** Process received signal ***
[fv-az1315-757:07990] Signal: Aborted (6)
[fv-az1315-757:07990] Signal code:  (-6)
[fv-az1315-757:07990] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feb20245330]
[fv-az1315-757:07990] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feb2029eb2c]
[fv-az1315-757:07990] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feb2024527e]
[fv-az1315-757:07990] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feb202288ff]
[fv-az1315-757:07990] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feb206a5ff5]
[fv-az1315-757:07990] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feb206bb0da]
[fv-az1315-757:07990] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feb206a5a55]
[fv-az1315-757:07990] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feb206a5a6f]
[fv-az1315-757:07990] [ 8] plumed(+0x13209)[0x55bd85b57209]
[fv-az1315-757:07990] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feb2022a1ca]
[fv-az1315-757:07990] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feb2022a28b]
[fv-az1315-757:07990] [11] plumed(+0x134a5)[0x55bd85b574a5]
[fv-az1315-757:07990] *** End of error message ***
</pre>
{% endraw %}
