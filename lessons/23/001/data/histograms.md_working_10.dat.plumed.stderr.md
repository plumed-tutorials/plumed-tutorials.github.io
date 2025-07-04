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
[pkrvmbietmlfzoi:36993] *** Process received signal ***
[pkrvmbietmlfzoi:36993] Signal: Aborted (6)
[pkrvmbietmlfzoi:36993] Signal code:  (-6)
[pkrvmbietmlfzoi:36993] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fac9ca45330]
[pkrvmbietmlfzoi:36993] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fac9ca9eb2c]
[pkrvmbietmlfzoi:36993] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fac9ca4527e]
[pkrvmbietmlfzoi:36993] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fac9ca288ff]
[pkrvmbietmlfzoi:36993] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fac9cea5ff5]
[pkrvmbietmlfzoi:36993] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fac9cebb0da]
[pkrvmbietmlfzoi:36993] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fac9cea5a55]
[pkrvmbietmlfzoi:36993] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fac9cea5a6f]
[pkrvmbietmlfzoi:36993] [ 8] plumed(+0x13209)[0x5633c1818209]
[pkrvmbietmlfzoi:36993] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fac9ca2a1ca]
[pkrvmbietmlfzoi:36993] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fac9ca2a28b]
[pkrvmbietmlfzoi:36993] [11] plumed(+0x134a5)[0x5633c18184a5]
[pkrvmbietmlfzoi:36993] *** End of error message ***
</pre>
{% endraw %}
