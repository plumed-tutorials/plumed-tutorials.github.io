Stderr for source:  examples.md_working_1.dat   
Download: [zipped raw stdout](examples.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1227) void PLMD::PlumedMain::load(const std::string&)
I cannot load library /path/to/PythonCVInterface.so /path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[pkrvmbietmlfzoi:35243] *** Process received signal ***
[pkrvmbietmlfzoi:35243] Signal: Aborted (6)
[pkrvmbietmlfzoi:35243] Signal code:  (-6)
[pkrvmbietmlfzoi:35243] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f79a2a45330]
[pkrvmbietmlfzoi:35243] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f79a2a9eb2c]
[pkrvmbietmlfzoi:35243] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f79a2a4527e]
[pkrvmbietmlfzoi:35243] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f79a2a288ff]
[pkrvmbietmlfzoi:35243] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f79a2ea5ff5]
[pkrvmbietmlfzoi:35243] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f79a2ebb0da]
[pkrvmbietmlfzoi:35243] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f79a2ea5a55]
[pkrvmbietmlfzoi:35243] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f79a2ea5a6f]
[pkrvmbietmlfzoi:35243] [ 8] plumed(+0x13209)[0x55fdfee0f209]
[pkrvmbietmlfzoi:35243] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f79a2a2a1ca]
[pkrvmbietmlfzoi:35243] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f79a2a2a28b]
[pkrvmbietmlfzoi:35243] [11] plumed(+0x134a5)[0x55fdfee0f4a5]
[pkrvmbietmlfzoi:35243] *** End of error message ***
</pre>
{% endraw %}
