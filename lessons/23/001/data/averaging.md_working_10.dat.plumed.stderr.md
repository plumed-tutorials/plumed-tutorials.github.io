Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36656] *** Process received signal ***
[pkrvmbietmlfzoi:36656] Signal: Aborted (6)
[pkrvmbietmlfzoi:36656] Signal code:  (-6)
[pkrvmbietmlfzoi:36656] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f29fea45330]
[pkrvmbietmlfzoi:36656] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f29fea9eb2c]
[pkrvmbietmlfzoi:36656] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f29fea4527e]
[pkrvmbietmlfzoi:36656] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f29fea288ff]
[pkrvmbietmlfzoi:36656] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f29feea5ff5]
[pkrvmbietmlfzoi:36656] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f29feebb0da]
[pkrvmbietmlfzoi:36656] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f29feea5a55]
[pkrvmbietmlfzoi:36656] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f29feea5a6f]
[pkrvmbietmlfzoi:36656] [ 8] plumed(+0x13209)[0x56304b9a3209]
[pkrvmbietmlfzoi:36656] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f29fea2a1ca]
[pkrvmbietmlfzoi:36656] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f29fea2a28b]
[pkrvmbietmlfzoi:36656] [11] plumed(+0x134a5)[0x56304b9a34a5]
[pkrvmbietmlfzoi:36656] *** End of error message ***
</pre>
{% endraw %}
