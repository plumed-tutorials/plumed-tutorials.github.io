Stderr for source:  averaging.md_working_4.dat   
Download: [zipped raw stdout](averaging.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1 CLEAR=100
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36477] *** Process received signal ***
[pkrvmbietmlfzoi:36477] Signal: Aborted (6)
[pkrvmbietmlfzoi:36477] Signal code:  (-6)
[pkrvmbietmlfzoi:36477] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff55a045330]
[pkrvmbietmlfzoi:36477] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff55a09eb2c]
[pkrvmbietmlfzoi:36477] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff55a04527e]
[pkrvmbietmlfzoi:36477] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff55a0288ff]
[pkrvmbietmlfzoi:36477] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff55a4a5ff5]
[pkrvmbietmlfzoi:36477] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff55a4bb0da]
[pkrvmbietmlfzoi:36477] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff55a4a5a55]
[pkrvmbietmlfzoi:36477] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff55a4a5a6f]
[pkrvmbietmlfzoi:36477] [ 8] plumed(+0x13209)[0x55e13df14209]
[pkrvmbietmlfzoi:36477] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff55a02a1ca]
[pkrvmbietmlfzoi:36477] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff55a02a28b]
[pkrvmbietmlfzoi:36477] [11] plumed(+0x134a5)[0x55e13df144a5]
[pkrvmbietmlfzoi:36477] *** End of error message ***
</pre>
{% endraw %}
