Stderr for source:  GAT_SAFE_README.md_working_3.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cv1 ATOMS=@mdatoms IMPORT=pycvPersistentData CALCULATE=pydist INIT=pyinit
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35192] *** Process received signal ***
[pkrvmbietmlfzoi:35192] Signal: Aborted (6)
[pkrvmbietmlfzoi:35192] Signal code:  (-6)
[pkrvmbietmlfzoi:35192] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd86e045330]
[pkrvmbietmlfzoi:35192] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd86e09eb2c]
[pkrvmbietmlfzoi:35192] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd86e04527e]
[pkrvmbietmlfzoi:35192] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd86e0288ff]
[pkrvmbietmlfzoi:35192] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd86e4a5ff5]
[pkrvmbietmlfzoi:35192] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd86e4bb0da]
[pkrvmbietmlfzoi:35192] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd86e4a5a55]
[pkrvmbietmlfzoi:35192] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd86e4a5a6f]
[pkrvmbietmlfzoi:35192] [ 8] plumed(+0x13209)[0x55d271e9f209]
[pkrvmbietmlfzoi:35192] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd86e02a1ca]
[pkrvmbietmlfzoi:35192] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd86e02a28b]
[pkrvmbietmlfzoi:35192] [11] plumed(+0x134a5)[0x55d271e9f4a5]
[pkrvmbietmlfzoi:35192] *** End of error message ***
</pre>
{% endraw %}
