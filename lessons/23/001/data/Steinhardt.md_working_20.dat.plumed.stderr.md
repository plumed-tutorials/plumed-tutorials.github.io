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
[fv-az1315-757:06902] *** Process received signal ***
[fv-az1315-757:06902] Signal: Aborted (6)
[fv-az1315-757:06902] Signal code:  (-6)
[fv-az1315-757:06902] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f28f4a45330]
[fv-az1315-757:06902] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f28f4a9eb2c]
[fv-az1315-757:06902] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f28f4a4527e]
[fv-az1315-757:06902] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f28f4a288ff]
[fv-az1315-757:06902] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f28f4ea5ff5]
[fv-az1315-757:06902] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f28f4ebb0da]
[fv-az1315-757:06902] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f28f4ea5a55]
[fv-az1315-757:06902] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f28f4ea5a6f]
[fv-az1315-757:06902] [ 8] plumed(+0x13209)[0x55f78ccc0209]
[fv-az1315-757:06902] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f28f4a2a1ca]
[fv-az1315-757:06902] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f28f4a2a28b]
[fv-az1315-757:06902] [11] plumed(+0x134a5)[0x55f78ccc04a5]
[fv-az1315-757:06902] *** End of error message ***
</pre>
{% endraw %}
