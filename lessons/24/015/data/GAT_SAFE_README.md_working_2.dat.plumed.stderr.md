Stderr for source:  GAT_SAFE_README.md_working_2.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYFUNCTION LABEL=fPY IMPORT=pycvfunc CALCULATE=plumedCalculate ARG=d1,d2
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35147] *** Process received signal ***
[pkrvmbietmlfzoi:35147] Signal: Aborted (6)
[pkrvmbietmlfzoi:35147] Signal code:  (-6)
[pkrvmbietmlfzoi:35147] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5c1e245330]
[pkrvmbietmlfzoi:35147] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5c1e29eb2c]
[pkrvmbietmlfzoi:35147] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5c1e24527e]
[pkrvmbietmlfzoi:35147] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5c1e2288ff]
[pkrvmbietmlfzoi:35147] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5c1e6a5ff5]
[pkrvmbietmlfzoi:35147] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5c1e6bb0da]
[pkrvmbietmlfzoi:35147] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5c1e6a5a55]
[pkrvmbietmlfzoi:35147] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5c1e6a5a6f]
[pkrvmbietmlfzoi:35147] [ 8] plumed(+0x13209)[0x55c63c7da209]
[pkrvmbietmlfzoi:35147] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5c1e22a1ca]
[pkrvmbietmlfzoi:35147] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5c1e22a28b]
[pkrvmbietmlfzoi:35147] [11] plumed(+0x134a5)[0x55c63c7da4a5]
[pkrvmbietmlfzoi:35147] *** End of error message ***
</pre>
{% endraw %}
