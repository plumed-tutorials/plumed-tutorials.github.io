Stderr for source:  Steinhardt.md_working_19.dat   
Download: [zipped raw stdout](Steinhardt.md_working_19.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_19.dat.plumed.stderr.txt.zip) 
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
[fv-az1315-757:06871] *** Process received signal ***
[fv-az1315-757:06871] Signal: Aborted (6)
[fv-az1315-757:06871] Signal code:  (-6)
[fv-az1315-757:06871] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f179ac45330]
[fv-az1315-757:06871] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f179ac9eb2c]
[fv-az1315-757:06871] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f179ac4527e]
[fv-az1315-757:06871] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f179ac288ff]
[fv-az1315-757:06871] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f179b0a5ff5]
[fv-az1315-757:06871] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f179b0bb0da]
[fv-az1315-757:06871] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f179b0a5a55]
[fv-az1315-757:06871] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f179b0a5a6f]
[fv-az1315-757:06871] [ 8] plumed(+0x13209)[0x559421774209]
[fv-az1315-757:06871] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f179ac2a1ca]
[fv-az1315-757:06871] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f179ac2a28b]
[fv-az1315-757:06871] [11] plumed(+0x134a5)[0x5594217744a5]
[fv-az1315-757:06871] *** End of error message ***
</pre>
{% endraw %}
