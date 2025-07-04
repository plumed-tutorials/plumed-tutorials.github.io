Stderr for source:  averaging.md_working_3.dat   
Download: [zipped raw stdout](averaging.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36446] *** Process received signal ***
[pkrvmbietmlfzoi:36446] Signal: Aborted (6)
[pkrvmbietmlfzoi:36446] Signal code:  (-6)
[pkrvmbietmlfzoi:36446] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f336b845330]
[pkrvmbietmlfzoi:36446] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f336b89eb2c]
[pkrvmbietmlfzoi:36446] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f336b84527e]
[pkrvmbietmlfzoi:36446] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f336b8288ff]
[pkrvmbietmlfzoi:36446] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f336bca5ff5]
[pkrvmbietmlfzoi:36446] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f336bcbb0da]
[pkrvmbietmlfzoi:36446] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f336bca5a55]
[pkrvmbietmlfzoi:36446] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f336bca5a6f]
[pkrvmbietmlfzoi:36446] [ 8] plumed(+0x13209)[0x55d47567e209]
[pkrvmbietmlfzoi:36446] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f336b82a1ca]
[pkrvmbietmlfzoi:36446] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f336b82a28b]
[pkrvmbietmlfzoi:36446] [11] plumed(+0x134a5)[0x55d47567e4a5]
[pkrvmbietmlfzoi:36446] *** End of error message ***
</pre>
{% endraw %}
