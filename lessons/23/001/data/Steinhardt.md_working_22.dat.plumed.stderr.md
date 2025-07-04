Stderr for source:  Steinhardt.md_working_22.dat   
Download: [zipped raw stdout](Steinhardt.md_working_22.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_22.dat.plumed.stderr.txt.zip) 
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
[pkrvmbietmlfzoi:35935] *** Process received signal ***
[pkrvmbietmlfzoi:35935] Signal: Aborted (6)
[pkrvmbietmlfzoi:35935] Signal code:  (-6)
[pkrvmbietmlfzoi:35935] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2f4b845330]
[pkrvmbietmlfzoi:35935] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2f4b89eb2c]
[pkrvmbietmlfzoi:35935] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2f4b84527e]
[pkrvmbietmlfzoi:35935] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2f4b8288ff]
[pkrvmbietmlfzoi:35935] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2f4bca5ff5]
[pkrvmbietmlfzoi:35935] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2f4bcbb0da]
[pkrvmbietmlfzoi:35935] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2f4bca5a55]
[pkrvmbietmlfzoi:35935] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2f4bca5a6f]
[pkrvmbietmlfzoi:35935] [ 8] plumed(+0x13209)[0x559ba2102209]
[pkrvmbietmlfzoi:35935] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2f4b82a1ca]
[pkrvmbietmlfzoi:35935] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2f4b82a28b]
[pkrvmbietmlfzoi:35935] [11] plumed(+0x134a5)[0x559ba21024a5]
[pkrvmbietmlfzoi:35935] *** End of error message ***
</pre>
{% endraw %}
