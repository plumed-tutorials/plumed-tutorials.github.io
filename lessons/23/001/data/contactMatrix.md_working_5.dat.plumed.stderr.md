Stderr for source:  contactMatrix.md_working_5.dat   
Download: [zipped raw stdout](contactMatrix.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:34999] *** Process received signal ***
[pkrvmbietmlfzoi:34999] Signal: Aborted (6)
[pkrvmbietmlfzoi:34999] Signal code:  (-6)
[pkrvmbietmlfzoi:34999] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f51ace45330]
[pkrvmbietmlfzoi:34999] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f51ace9eb2c]
[pkrvmbietmlfzoi:34999] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f51ace4527e]
[pkrvmbietmlfzoi:34999] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f51ace288ff]
[pkrvmbietmlfzoi:34999] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f51ad2a5ff5]
[pkrvmbietmlfzoi:34999] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f51ad2bb0da]
[pkrvmbietmlfzoi:34999] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f51ad2a5a55]
[pkrvmbietmlfzoi:34999] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f51ad2a5a6f]
[pkrvmbietmlfzoi:34999] [ 8] plumed(+0x13209)[0x55def9513209]
[pkrvmbietmlfzoi:34999] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f51ace2a1ca]
[pkrvmbietmlfzoi:34999] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f51ace2a28b]
[pkrvmbietmlfzoi:34999] [11] plumed(+0x134a5)[0x55def95134a5]
[pkrvmbietmlfzoi:34999] *** End of error message ***
</pre>
{% endraw %}
