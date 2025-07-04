Stderr for source:  histograms.md_working_6.dat   
Download: [zipped raw stdout](histograms.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: RDF LABEL=rdf GROUP=1-1000 GRID_BIN=100 MAXR=1.0 BANDWIDTH=0.01
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36850] *** Process received signal ***
[pkrvmbietmlfzoi:36850] Signal: Aborted (6)
[pkrvmbietmlfzoi:36850] Signal code:  (-6)
[pkrvmbietmlfzoi:36850] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efd05645330]
[pkrvmbietmlfzoi:36850] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efd0569eb2c]
[pkrvmbietmlfzoi:36850] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efd0564527e]
[pkrvmbietmlfzoi:36850] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efd056288ff]
[pkrvmbietmlfzoi:36850] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efd05aa5ff5]
[pkrvmbietmlfzoi:36850] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efd05abb0da]
[pkrvmbietmlfzoi:36850] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efd05aa5a55]
[pkrvmbietmlfzoi:36850] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efd05aa5a6f]
[pkrvmbietmlfzoi:36850] [ 8] plumed(+0x13209)[0x558db3225209]
[pkrvmbietmlfzoi:36850] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efd0562a1ca]
[pkrvmbietmlfzoi:36850] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efd0562a28b]
[pkrvmbietmlfzoi:36850] [11] plumed(+0x134a5)[0x558db32254a5]
[pkrvmbietmlfzoi:36850] *** End of error message ***
</pre>
{% endraw %}
