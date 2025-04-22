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
[fv-az1315-757:08102] *** Process received signal ***
[fv-az1315-757:08102] Signal: Aborted (6)
[fv-az1315-757:08102] Signal code:  (-6)
[fv-az1315-757:08102] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f929f045330]
[fv-az1315-757:08102] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f929f09eb2c]
[fv-az1315-757:08102] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f929f04527e]
[fv-az1315-757:08102] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f929f0288ff]
[fv-az1315-757:08102] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f929f4a5ff5]
[fv-az1315-757:08102] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f929f4bb0da]
[fv-az1315-757:08102] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f929f4a5a55]
[fv-az1315-757:08102] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f929f4a5a6f]
[fv-az1315-757:08102] [ 8] plumed(+0x13209)[0x5637afe77209]
[fv-az1315-757:08102] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f929f02a1ca]
[fv-az1315-757:08102] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f929f02a28b]
[fv-az1315-757:08102] [11] plumed(+0x134a5)[0x5637afe774a5]
[fv-az1315-757:08102] *** End of error message ***
</pre>
{% endraw %}
