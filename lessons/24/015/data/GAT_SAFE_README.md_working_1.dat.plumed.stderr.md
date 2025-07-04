Stderr for source:  GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cvPY ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35102] *** Process received signal ***
[pkrvmbietmlfzoi:35102] Signal: Aborted (6)
[pkrvmbietmlfzoi:35102] Signal code:  (-6)
[pkrvmbietmlfzoi:35102] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0680845330]
[pkrvmbietmlfzoi:35102] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f068089eb2c]
[pkrvmbietmlfzoi:35102] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f068084527e]
[pkrvmbietmlfzoi:35102] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f06808288ff]
[pkrvmbietmlfzoi:35102] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0680ca5ff5]
[pkrvmbietmlfzoi:35102] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0680cbb0da]
[pkrvmbietmlfzoi:35102] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0680ca5a55]
[pkrvmbietmlfzoi:35102] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0680ca5a6f]
[pkrvmbietmlfzoi:35102] [ 8] plumed(+0x13209)[0x55a514887209]
[pkrvmbietmlfzoi:35102] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f068082a1ca]
[pkrvmbietmlfzoi:35102] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f068082a28b]
[pkrvmbietmlfzoi:35102] [11] plumed(+0x134a5)[0x55a5148874a5]
[pkrvmbietmlfzoi:35102] *** End of error message ***
</pre>
{% endraw %}
