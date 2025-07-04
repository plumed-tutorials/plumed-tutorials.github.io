Stderr for source:  averaging.md_working_6.dat   
Download: [zipped raw stdout](averaging.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36526] *** Process received signal ***
[pkrvmbietmlfzoi:36526] Signal: Aborted (6)
[pkrvmbietmlfzoi:36526] Signal code:  (-6)
[pkrvmbietmlfzoi:36526] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f201ee45330]
[pkrvmbietmlfzoi:36526] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f201ee9eb2c]
[pkrvmbietmlfzoi:36526] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f201ee4527e]
[pkrvmbietmlfzoi:36526] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f201ee288ff]
[pkrvmbietmlfzoi:36526] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f201f2a5ff5]
[pkrvmbietmlfzoi:36526] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f201f2bb0da]
[pkrvmbietmlfzoi:36526] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f201f2a5a55]
[pkrvmbietmlfzoi:36526] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f201f2a5a6f]
[pkrvmbietmlfzoi:36526] [ 8] plumed(+0x13209)[0x55b2a55b1209]
[pkrvmbietmlfzoi:36526] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f201ee2a1ca]
[pkrvmbietmlfzoi:36526] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f201ee2a28b]
[pkrvmbietmlfzoi:36526] [11] plumed(+0x134a5)[0x55b2a55b14a5]
[pkrvmbietmlfzoi:36526] *** End of error message ***
</pre>
{% endraw %}
