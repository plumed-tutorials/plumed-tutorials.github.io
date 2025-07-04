Stderr for source:  Tasks.md_working_3.dat   
Download: [zipped raw stdout](Tasks.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones SIZE=100
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35106] *** Process received signal ***
[pkrvmbietmlfzoi:35106] Signal: Aborted (6)
[pkrvmbietmlfzoi:35106] Signal code:  (-6)
[pkrvmbietmlfzoi:35106] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fea65045330]
[pkrvmbietmlfzoi:35106] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fea6509eb2c]
[pkrvmbietmlfzoi:35106] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fea6504527e]
[pkrvmbietmlfzoi:35106] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fea650288ff]
[pkrvmbietmlfzoi:35106] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fea654a5ff5]
[pkrvmbietmlfzoi:35106] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fea654bb0da]
[pkrvmbietmlfzoi:35106] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fea654a5a55]
[pkrvmbietmlfzoi:35106] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fea654a5a6f]
[pkrvmbietmlfzoi:35106] [ 8] plumed(+0x13209)[0x55f7425b8209]
[pkrvmbietmlfzoi:35106] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fea6502a1ca]
[pkrvmbietmlfzoi:35106] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fea6502a28b]
[pkrvmbietmlfzoi:35106] [11] plumed(+0x134a5)[0x55f7425b84a5]
[pkrvmbietmlfzoi:35106] *** End of error message ***
</pre>
{% endraw %}
