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
[runnervmg397c:80126] *** Process received signal ***
[runnervmg397c:80126] Signal: Aborted (6)
[runnervmg397c:80126] Signal code:  (-6)
[runnervmg397c:80126] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1fff445330]
[runnervmg397c:80126] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1fff49eb2c]
[runnervmg397c:80126] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1fff44527e]
[runnervmg397c:80126] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1fff4288ff]
[runnervmg397c:80126] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1fff8a5ff5]
[runnervmg397c:80126] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1fff8bb0da]
[runnervmg397c:80126] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1fff8a5a55]
[runnervmg397c:80126] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1fff8a5a6f]
[runnervmg397c:80126] [ 8] plumed(+0x13209)[0x55bf3a609209]
[runnervmg397c:80126] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1fff42a1ca]
[runnervmg397c:80126] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1fff42a28b]
[runnervmg397c:80126] [11] plumed(+0x134a5)[0x55bf3a6094a5]
[runnervmg397c:80126] *** End of error message ***
</pre>
{% endraw %}
