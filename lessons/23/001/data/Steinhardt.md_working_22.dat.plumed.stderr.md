Stderr for source:  Steinhardt.md_working_22.dat   
Download: [zipped raw stdout](Steinhardt.md_working_22.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_22.dat.plumed.stderr.txt.zip) 
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
[fv-az1315-757:06965] *** Process received signal ***
[fv-az1315-757:06965] Signal: Aborted (6)
[fv-az1315-757:06965] Signal code:  (-6)
[fv-az1315-757:06965] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1aac045330]
[fv-az1315-757:06965] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1aac09eb2c]
[fv-az1315-757:06965] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1aac04527e]
[fv-az1315-757:06965] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1aac0288ff]
[fv-az1315-757:06965] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1aac4a5ff5]
[fv-az1315-757:06965] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1aac4bb0da]
[fv-az1315-757:06965] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1aac4a5a55]
[fv-az1315-757:06965] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1aac4a5a6f]
[fv-az1315-757:06965] [ 8] plumed(+0x13209)[0x55f2cec8a209]
[fv-az1315-757:06965] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1aac02a1ca]
[fv-az1315-757:06965] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1aac02a28b]
[fv-az1315-757:06965] [11] plumed(+0x134a5)[0x55f2cec8a4a5]
[fv-az1315-757:06965] *** End of error message ***
</pre>
{% endraw %}
