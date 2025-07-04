Stderr for source:  histograms.md_working_11.dat   
Download: [zipped raw stdout](histograms.md_working_11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1 HEIGHTS=one
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:37026] *** Process received signal ***
[pkrvmbietmlfzoi:37026] Signal: Aborted (6)
[pkrvmbietmlfzoi:37026] Signal code:  (-6)
[pkrvmbietmlfzoi:37026] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f81e0645330]
[pkrvmbietmlfzoi:37026] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f81e069eb2c]
[pkrvmbietmlfzoi:37026] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f81e064527e]
[pkrvmbietmlfzoi:37026] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f81e06288ff]
[pkrvmbietmlfzoi:37026] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f81e0aa5ff5]
[pkrvmbietmlfzoi:37026] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f81e0abb0da]
[pkrvmbietmlfzoi:37026] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f81e0aa5a55]
[pkrvmbietmlfzoi:37026] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f81e0aa5a6f]
[pkrvmbietmlfzoi:37026] [ 8] plumed(+0x13209)[0x55cb78bc6209]
[pkrvmbietmlfzoi:37026] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f81e062a1ca]
[pkrvmbietmlfzoi:37026] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f81e062a28b]
[pkrvmbietmlfzoi:37026] [11] plumed(+0x134a5)[0x55cb78bc64a5]
[pkrvmbietmlfzoi:37026] *** End of error message ***
</pre>
{% endraw %}
