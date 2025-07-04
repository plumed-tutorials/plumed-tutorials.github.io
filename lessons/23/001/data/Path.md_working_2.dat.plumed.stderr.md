Stderr for source:  Path.md_working_2.dat   
Download: [zipped raw stdout](Path.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: LOWEST LABEL=p_mindist ARG=p_data
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:37472] *** Process received signal ***
[pkrvmbietmlfzoi:37472] Signal: Aborted (6)
[pkrvmbietmlfzoi:37472] Signal code:  (-6)
[pkrvmbietmlfzoi:37472] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc3a7645330]
[pkrvmbietmlfzoi:37472] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc3a769eb2c]
[pkrvmbietmlfzoi:37472] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc3a764527e]
[pkrvmbietmlfzoi:37472] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc3a76288ff]
[pkrvmbietmlfzoi:37472] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc3a7aa5ff5]
[pkrvmbietmlfzoi:37472] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc3a7abb0da]
[pkrvmbietmlfzoi:37472] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc3a7aa5a55]
[pkrvmbietmlfzoi:37472] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc3a7aa5a6f]
[pkrvmbietmlfzoi:37472] [ 8] plumed(+0x13209)[0x559626cee209]
[pkrvmbietmlfzoi:37472] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc3a762a1ca]
[pkrvmbietmlfzoi:37472] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc3a762a28b]
[pkrvmbietmlfzoi:37472] [11] plumed(+0x134a5)[0x559626cee4a5]
[pkrvmbietmlfzoi:37472] *** End of error message ***
</pre>
{% endraw %}
