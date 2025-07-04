Stderr for source:  Steinhardt.md_working_4.dat   
Download: [zipped raw stdout](Steinhardt.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIESA=1 SPECIESB=2-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35364] *** Process received signal ***
[pkrvmbietmlfzoi:35364] Signal: Aborted (6)
[pkrvmbietmlfzoi:35364] Signal code:  (-6)
[pkrvmbietmlfzoi:35364] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa6eb445330]
[pkrvmbietmlfzoi:35364] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa6eb49eb2c]
[pkrvmbietmlfzoi:35364] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa6eb44527e]
[pkrvmbietmlfzoi:35364] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa6eb4288ff]
[pkrvmbietmlfzoi:35364] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa6eb8a5ff5]
[pkrvmbietmlfzoi:35364] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa6eb8bb0da]
[pkrvmbietmlfzoi:35364] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa6eb8a5a55]
[pkrvmbietmlfzoi:35364] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa6eb8a5a6f]
[pkrvmbietmlfzoi:35364] [ 8] plumed(+0x13209)[0x55f8d7091209]
[pkrvmbietmlfzoi:35364] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa6eb42a1ca]
[pkrvmbietmlfzoi:35364] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa6eb42a28b]
[pkrvmbietmlfzoi:35364] [11] plumed(+0x134a5)[0x55f8d70914a5]
[pkrvmbietmlfzoi:35364] *** End of error message ***
</pre>
{% endraw %}
