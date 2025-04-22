Stderr for source:  contactMatrix.md_working_6.dat   
Download: [zipped raw stdout](contactMatrix.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[fv-az1315-757:05934] *** Process received signal ***
[fv-az1315-757:05934] Signal: Aborted (6)
[fv-az1315-757:05934] Signal code:  (-6)
[fv-az1315-757:05934] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f641a245330]
[fv-az1315-757:05934] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f641a29eb2c]
[fv-az1315-757:05934] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f641a24527e]
[fv-az1315-757:05934] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f641a2288ff]
[fv-az1315-757:05934] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f641a6a5ff5]
[fv-az1315-757:05934] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f641a6bb0da]
[fv-az1315-757:05934] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f641a6a5a55]
[fv-az1315-757:05934] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f641a6a5a6f]
[fv-az1315-757:05934] [ 8] plumed(+0x13209)[0x564184ee5209]
[fv-az1315-757:05934] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f641a22a1ca]
[fv-az1315-757:05934] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f641a22a28b]
[fv-az1315-757:05934] [11] plumed(+0x134a5)[0x564184ee54a5]
[fv-az1315-757:05934] *** End of error message ***
</pre>
{% endraw %}
