Stderr for source:  work/plumed_ex10.dat   
Download: [zipped raw stdout](plumed_ex10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36238] *** Process received signal ***
[pkrvmbietmlfzoi:36238] Signal: Aborted (6)
[pkrvmbietmlfzoi:36238] Signal code:  (-6)
[pkrvmbietmlfzoi:36238] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc75fa45330]
[pkrvmbietmlfzoi:36238] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc75fa9eb2c]
[pkrvmbietmlfzoi:36238] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc75fa4527e]
[pkrvmbietmlfzoi:36238] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc75fa288ff]
[pkrvmbietmlfzoi:36238] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc75fea5ff5]
[pkrvmbietmlfzoi:36238] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc75febb0da]
[pkrvmbietmlfzoi:36238] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc75fea5a55]
[pkrvmbietmlfzoi:36238] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc75fea5a6f]
[pkrvmbietmlfzoi:36238] [ 8] plumed(+0x13209)[0x55a5e5db2209]
[pkrvmbietmlfzoi:36238] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc75fa2a1ca]
[pkrvmbietmlfzoi:36238] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc75fa2a28b]
[pkrvmbietmlfzoi:36238] [11] plumed(+0x134a5)[0x55a5e5db24a5]
[pkrvmbietmlfzoi:36238] *** End of error message ***
</pre>
{% endraw %}
