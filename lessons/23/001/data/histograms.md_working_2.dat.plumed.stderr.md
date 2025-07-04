Stderr for source:  histograms.md_working_2.dat   
Download: [zipped raw stdout](histograms.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_2.dat.plumed.stderr.txt.zip) 
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
[pkrvmbietmlfzoi:36724] *** Process received signal ***
[pkrvmbietmlfzoi:36724] Signal: Aborted (6)
[pkrvmbietmlfzoi:36724] Signal code:  (-6)
[pkrvmbietmlfzoi:36724] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f691a245330]
[pkrvmbietmlfzoi:36724] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f691a29eb2c]
[pkrvmbietmlfzoi:36724] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f691a24527e]
[pkrvmbietmlfzoi:36724] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f691a2288ff]
[pkrvmbietmlfzoi:36724] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f691a6a5ff5]
[pkrvmbietmlfzoi:36724] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f691a6bb0da]
[pkrvmbietmlfzoi:36724] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f691a6a5a55]
[pkrvmbietmlfzoi:36724] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f691a6a5a6f]
[pkrvmbietmlfzoi:36724] [ 8] plumed(+0x13209)[0x559ef5f9a209]
[pkrvmbietmlfzoi:36724] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f691a22a1ca]
[pkrvmbietmlfzoi:36724] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f691a22a28b]
[pkrvmbietmlfzoi:36724] [11] plumed(+0x134a5)[0x559ef5f9a4a5]
[pkrvmbietmlfzoi:36724] *** End of error message ***
</pre>
{% endraw %}
