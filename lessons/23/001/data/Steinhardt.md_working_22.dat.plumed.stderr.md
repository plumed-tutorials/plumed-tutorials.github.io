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
[runnervmg397c:80188] *** Process received signal ***
[runnervmg397c:80188] Signal: Aborted (6)
[runnervmg397c:80188] Signal code:  (-6)
[runnervmg397c:80188] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f754ce45330]
[runnervmg397c:80188] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f754ce9eb2c]
[runnervmg397c:80188] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f754ce4527e]
[runnervmg397c:80188] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f754ce288ff]
[runnervmg397c:80188] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f754d2a5ff5]
[runnervmg397c:80188] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f754d2bb0da]
[runnervmg397c:80188] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f754d2a5a55]
[runnervmg397c:80188] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f754d2a5a6f]
[runnervmg397c:80188] [ 8] plumed(+0x13209)[0x5563ecccd209]
[runnervmg397c:80188] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f754ce2a1ca]
[runnervmg397c:80188] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f754ce2a28b]
[runnervmg397c:80188] [11] plumed(+0x134a5)[0x5563ecccd4a5]
[runnervmg397c:80188] *** End of error message ***
</pre>
{% endraw %}
