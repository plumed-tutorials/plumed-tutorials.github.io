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
[pkrvmbietmlfzoi:36756] *** Process received signal ***
[pkrvmbietmlfzoi:36756] Signal: Aborted (6)
[pkrvmbietmlfzoi:36756] Signal code:  (-6)
[pkrvmbietmlfzoi:36756] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbcdb245330]
[pkrvmbietmlfzoi:36756] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbcdb29eb2c]
[pkrvmbietmlfzoi:36756] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbcdb24527e]
[pkrvmbietmlfzoi:36756] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbcdb2288ff]
[pkrvmbietmlfzoi:36756] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbcdb6a5ff5]
[pkrvmbietmlfzoi:36756] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbcdb6bb0da]
[pkrvmbietmlfzoi:36756] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbcdb6a5a55]
[pkrvmbietmlfzoi:36756] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbcdb6a5a6f]
[pkrvmbietmlfzoi:36756] [ 8] plumed(+0x13209)[0x55f4b242a209]
[pkrvmbietmlfzoi:36756] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbcdb22a1ca]
[pkrvmbietmlfzoi:36756] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbcdb22a28b]
[pkrvmbietmlfzoi:36756] [11] plumed(+0x134a5)[0x55f4b242a4a5]
[pkrvmbietmlfzoi:36756] *** End of error message ***
</pre>
{% endraw %}
