Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36576] *** Process received signal ***
[pkrvmbietmlfzoi:36576] Signal: Aborted (6)
[pkrvmbietmlfzoi:36576] Signal code:  (-6)
[pkrvmbietmlfzoi:36576] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f02cb445330]
[pkrvmbietmlfzoi:36576] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f02cb49eb2c]
[pkrvmbietmlfzoi:36576] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f02cb44527e]
[pkrvmbietmlfzoi:36576] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f02cb4288ff]
[pkrvmbietmlfzoi:36576] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f02cb8a5ff5]
[pkrvmbietmlfzoi:36576] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f02cb8bb0da]
[pkrvmbietmlfzoi:36576] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f02cb8a5a55]
[pkrvmbietmlfzoi:36576] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f02cb8a5a6f]
[pkrvmbietmlfzoi:36576] [ 8] plumed(+0x13209)[0x557053974209]
[pkrvmbietmlfzoi:36576] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f02cb42a1ca]
[pkrvmbietmlfzoi:36576] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f02cb42a28b]
[pkrvmbietmlfzoi:36576] [11] plumed(+0x134a5)[0x5570539744a5]
[pkrvmbietmlfzoi:36576] *** End of error message ***
</pre>
{% endraw %}
