Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:37503] *** Process received signal ***
[pkrvmbietmlfzoi:37503] Signal: Aborted (6)
[pkrvmbietmlfzoi:37503] Signal code:  (-6)
[pkrvmbietmlfzoi:37503] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f714d445330]
[pkrvmbietmlfzoi:37503] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f714d49eb2c]
[pkrvmbietmlfzoi:37503] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f714d44527e]
[pkrvmbietmlfzoi:37503] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f714d4288ff]
[pkrvmbietmlfzoi:37503] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f714d8a5ff5]
[pkrvmbietmlfzoi:37503] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f714d8bb0da]
[pkrvmbietmlfzoi:37503] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f714d8a5a55]
[pkrvmbietmlfzoi:37503] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f714d8a5a6f]
[pkrvmbietmlfzoi:37503] [ 8] plumed(+0x13209)[0x56455b71d209]
[pkrvmbietmlfzoi:37503] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f714d42a1ca]
[pkrvmbietmlfzoi:37503] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f714d42a28b]
[pkrvmbietmlfzoi:37503] [11] plumed(+0x134a5)[0x56455b71d4a5]
[pkrvmbietmlfzoi:37503] *** End of error message ***
</pre>
{% endraw %}
