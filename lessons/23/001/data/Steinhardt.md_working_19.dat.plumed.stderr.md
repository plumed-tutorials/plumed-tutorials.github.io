Stderr for source:  Steinhardt.md_working_19.dat   
Download: [zipped raw stdout](Steinhardt.md_working_19.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_19.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35842] *** Process received signal ***
[pkrvmbietmlfzoi:35842] Signal: Aborted (6)
[pkrvmbietmlfzoi:35842] Signal code:  (-6)
[pkrvmbietmlfzoi:35842] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffa5f045330]
[pkrvmbietmlfzoi:35842] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffa5f09eb2c]
[pkrvmbietmlfzoi:35842] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffa5f04527e]
[pkrvmbietmlfzoi:35842] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffa5f0288ff]
[pkrvmbietmlfzoi:35842] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffa5f4a5ff5]
[pkrvmbietmlfzoi:35842] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffa5f4bb0da]
[pkrvmbietmlfzoi:35842] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffa5f4a5a55]
[pkrvmbietmlfzoi:35842] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffa5f4a5a6f]
[pkrvmbietmlfzoi:35842] [ 8] plumed(+0x13209)[0x555bfe5e6209]
[pkrvmbietmlfzoi:35842] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffa5f02a1ca]
[pkrvmbietmlfzoi:35842] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffa5f02a28b]
[pkrvmbietmlfzoi:35842] [11] plumed(+0x134a5)[0x555bfe5e64a5]
[pkrvmbietmlfzoi:35842] *** End of error message ***
</pre>
{% endraw %}
