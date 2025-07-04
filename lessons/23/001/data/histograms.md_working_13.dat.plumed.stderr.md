Stderr for source:  histograms.md_working_13.dat   
Download: [zipped raw stdout](histograms.md_working_13.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_13.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1 HEIGHTS=fh
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:37090] *** Process received signal ***
[pkrvmbietmlfzoi:37090] Signal: Aborted (6)
[pkrvmbietmlfzoi:37090] Signal code:  (-6)
[pkrvmbietmlfzoi:37090] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcbae645330]
[pkrvmbietmlfzoi:37090] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcbae69eb2c]
[pkrvmbietmlfzoi:37090] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcbae64527e]
[pkrvmbietmlfzoi:37090] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcbae6288ff]
[pkrvmbietmlfzoi:37090] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcbaeaa5ff5]
[pkrvmbietmlfzoi:37090] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcbaeabb0da]
[pkrvmbietmlfzoi:37090] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcbaeaa5a55]
[pkrvmbietmlfzoi:37090] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcbaeaa5a6f]
[pkrvmbietmlfzoi:37090] [ 8] plumed(+0x13209)[0x564e4eefa209]
[pkrvmbietmlfzoi:37090] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcbae62a1ca]
[pkrvmbietmlfzoi:37090] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcbae62a28b]
[pkrvmbietmlfzoi:37090] [11] plumed(+0x134a5)[0x564e4eefa4a5]
[pkrvmbietmlfzoi:37090] *** End of error message ***
</pre>
{% endraw %}
