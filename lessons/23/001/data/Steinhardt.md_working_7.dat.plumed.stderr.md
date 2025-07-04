Stderr for source:  Steinhardt.md_working_7.dat   
Download: [zipped raw stdout](Steinhardt.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 MEAN
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35458] *** Process received signal ***
[pkrvmbietmlfzoi:35458] Signal: Aborted (6)
[pkrvmbietmlfzoi:35458] Signal code:  (-6)
[pkrvmbietmlfzoi:35458] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6280a45330]
[pkrvmbietmlfzoi:35458] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6280a9eb2c]
[pkrvmbietmlfzoi:35458] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6280a4527e]
[pkrvmbietmlfzoi:35458] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6280a288ff]
[pkrvmbietmlfzoi:35458] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6280ea5ff5]
[pkrvmbietmlfzoi:35458] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6280ebb0da]
[pkrvmbietmlfzoi:35458] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6280ea5a55]
[pkrvmbietmlfzoi:35458] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6280ea5a6f]
[pkrvmbietmlfzoi:35458] [ 8] plumed(+0x13209)[0x55d190f43209]
[pkrvmbietmlfzoi:35458] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6280a2a1ca]
[pkrvmbietmlfzoi:35458] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6280a2a28b]
[pkrvmbietmlfzoi:35458] [11] plumed(+0x134a5)[0x55d190f434a5]
[pkrvmbietmlfzoi:35458] *** End of error message ***
</pre>
{% endraw %}
