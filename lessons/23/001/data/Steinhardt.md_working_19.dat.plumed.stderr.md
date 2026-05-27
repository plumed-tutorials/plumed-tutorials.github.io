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
[runnervmg397c:80089] *** Process received signal ***
[runnervmg397c:80089] Signal: Aborted (6)
[runnervmg397c:80089] Signal code:  (-6)
[runnervmg397c:80089] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5bcf045330]
[runnervmg397c:80089] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5bcf09eb2c]
[runnervmg397c:80089] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5bcf04527e]
[runnervmg397c:80089] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5bcf0288ff]
[runnervmg397c:80089] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5bcf4a5ff5]
[runnervmg397c:80089] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5bcf4bb0da]
[runnervmg397c:80089] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5bcf4a5a55]
[runnervmg397c:80089] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5bcf4a5a6f]
[runnervmg397c:80089] [ 8] plumed(+0x13209)[0x55de1f540209]
[runnervmg397c:80089] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5bcf02a1ca]
[runnervmg397c:80089] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5bcf02a28b]
[runnervmg397c:80089] [11] plumed(+0x134a5)[0x55de1f5404a5]
[runnervmg397c:80089] *** End of error message ***
</pre>
{% endraw %}
