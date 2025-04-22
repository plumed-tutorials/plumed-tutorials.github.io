Stderr for source:  Steinhardt.md_working_4.dat   
Download: [zipped raw stdout](Steinhardt.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIESA=1 SPECIESB=2-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[fv-az1315-757:06390] *** Process received signal ***
[fv-az1315-757:06390] Signal: Aborted (6)
[fv-az1315-757:06390] Signal code:  (-6)
[fv-az1315-757:06390] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa273845330]
[fv-az1315-757:06390] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa27389eb2c]
[fv-az1315-757:06390] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa27384527e]
[fv-az1315-757:06390] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa2738288ff]
[fv-az1315-757:06390] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa273ca5ff5]
[fv-az1315-757:06390] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa273cbb0da]
[fv-az1315-757:06390] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa273ca5a55]
[fv-az1315-757:06390] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa273ca5a6f]
[fv-az1315-757:06390] [ 8] plumed(+0x13209)[0x561a4afaf209]
[fv-az1315-757:06390] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa27382a1ca]
[fv-az1315-757:06390] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa27382a28b]
[fv-az1315-757:06390] [11] plumed(+0x134a5)[0x561a4afaf4a5]
[fv-az1315-757:06390] *** End of error message ***
</pre>
{% endraw %}
