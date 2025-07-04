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
[pkrvmbietmlfzoi:36881] *** Process received signal ***
[pkrvmbietmlfzoi:36881] Signal: Aborted (6)
[pkrvmbietmlfzoi:36881] Signal code:  (-6)
[pkrvmbietmlfzoi:36881] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f67dd845330]
[pkrvmbietmlfzoi:36881] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f67dd89eb2c]
[pkrvmbietmlfzoi:36881] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f67dd84527e]
[pkrvmbietmlfzoi:36881] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f67dd8288ff]
[pkrvmbietmlfzoi:36881] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f67ddca5ff5]
[pkrvmbietmlfzoi:36881] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f67ddcbb0da]
[pkrvmbietmlfzoi:36881] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f67ddca5a55]
[pkrvmbietmlfzoi:36881] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f67ddca5a6f]
[pkrvmbietmlfzoi:36881] [ 8] plumed(+0x13209)[0x55fe9a2ef209]
[pkrvmbietmlfzoi:36881] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f67dd82a1ca]
[pkrvmbietmlfzoi:36881] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f67dd82a28b]
[pkrvmbietmlfzoi:36881] [11] plumed(+0x134a5)[0x55fe9a2ef4a5]
[pkrvmbietmlfzoi:36881] *** End of error message ***
</pre>
{% endraw %}
