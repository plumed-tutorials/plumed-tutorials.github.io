Stderr for source:  Steinhardt.md_working_20.dat   
Download: [zipped raw stdout](Steinhardt.md_working_20.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_20.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35873] *** Process received signal ***
[pkrvmbietmlfzoi:35873] Signal: Aborted (6)
[pkrvmbietmlfzoi:35873] Signal code:  (-6)
[pkrvmbietmlfzoi:35873] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6c8ce45330]
[pkrvmbietmlfzoi:35873] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6c8ce9eb2c]
[pkrvmbietmlfzoi:35873] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6c8ce4527e]
[pkrvmbietmlfzoi:35873] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6c8ce288ff]
[pkrvmbietmlfzoi:35873] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6c8d2a5ff5]
[pkrvmbietmlfzoi:35873] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6c8d2bb0da]
[pkrvmbietmlfzoi:35873] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6c8d2a5a55]
[pkrvmbietmlfzoi:35873] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6c8d2a5a6f]
[pkrvmbietmlfzoi:35873] [ 8] plumed(+0x13209)[0x55ec27e1f209]
[pkrvmbietmlfzoi:35873] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6c8ce2a1ca]
[pkrvmbietmlfzoi:35873] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6c8ce2a28b]
[pkrvmbietmlfzoi:35873] [11] plumed(+0x134a5)[0x55ec27e1f4a5]
[pkrvmbietmlfzoi:35873] *** End of error message ***
</pre>
{% endraw %}
