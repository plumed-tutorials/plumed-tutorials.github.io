Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed.stderr.txt.zip) 
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
[pkrvmbietmlfzoi:36269] *** Process received signal ***
[pkrvmbietmlfzoi:36269] Signal: Aborted (6)
[pkrvmbietmlfzoi:36269] Signal code:  (-6)
[pkrvmbietmlfzoi:36269] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f98a1445330]
[pkrvmbietmlfzoi:36269] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f98a149eb2c]
[pkrvmbietmlfzoi:36269] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f98a144527e]
[pkrvmbietmlfzoi:36269] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f98a14288ff]
[pkrvmbietmlfzoi:36269] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f98a18a5ff5]
[pkrvmbietmlfzoi:36269] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f98a18bb0da]
[pkrvmbietmlfzoi:36269] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f98a18a5a55]
[pkrvmbietmlfzoi:36269] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f98a18a5a6f]
[pkrvmbietmlfzoi:36269] [ 8] plumed(+0x13209)[0x5600fe6d2209]
[pkrvmbietmlfzoi:36269] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f98a142a1ca]
[pkrvmbietmlfzoi:36269] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f98a142a28b]
[pkrvmbietmlfzoi:36269] [11] plumed(+0x134a5)[0x5600fe6d24a5]
[pkrvmbietmlfzoi:36269] *** End of error message ***
</pre>
{% endraw %}
