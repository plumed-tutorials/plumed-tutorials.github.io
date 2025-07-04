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
[pkrvmbietmlfzoi:36788] *** Process received signal ***
[pkrvmbietmlfzoi:36788] Signal: Aborted (6)
[pkrvmbietmlfzoi:36788] Signal code:  (-6)
[pkrvmbietmlfzoi:36788] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feba3445330]
[pkrvmbietmlfzoi:36788] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feba349eb2c]
[pkrvmbietmlfzoi:36788] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feba344527e]
[pkrvmbietmlfzoi:36788] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feba34288ff]
[pkrvmbietmlfzoi:36788] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feba38a5ff5]
[pkrvmbietmlfzoi:36788] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feba38bb0da]
[pkrvmbietmlfzoi:36788] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feba38a5a55]
[pkrvmbietmlfzoi:36788] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feba38a5a6f]
[pkrvmbietmlfzoi:36788] [ 8] plumed(+0x13209)[0x5583987f3209]
[pkrvmbietmlfzoi:36788] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feba342a1ca]
[pkrvmbietmlfzoi:36788] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feba342a28b]
[pkrvmbietmlfzoi:36788] [11] plumed(+0x134a5)[0x5583987f34a5]
[pkrvmbietmlfzoi:36788] *** End of error message ***
</pre>
{% endraw %}
