Stderr for source:  Steinhardt.md_working_7.dat   
Download: [zipped raw stdout](Steinhardt.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 MEAN
Maybe a missing space or a typo?
[runnervmg397c:79713] *** Process received signal ***
[runnervmg397c:79713] Signal: Aborted (6)
[runnervmg397c:79713] Signal code:  (-6)
[runnervmg397c:79713] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6f3f245330]
[runnervmg397c:79713] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6f3f29eb2c]
[runnervmg397c:79713] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6f3f24527e]
[runnervmg397c:79713] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6f3f2288ff]
[runnervmg397c:79713] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6f3f6a5ff5]
[runnervmg397c:79713] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6f3f6bb0da]
[runnervmg397c:79713] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6f3f6a5a55]
[runnervmg397c:79713] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6f3f6a5a6f]
[runnervmg397c:79713] [ 8] plumed(+0x13209)[0x5649de963209]
[runnervmg397c:79713] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6f3f22a1ca]
[runnervmg397c:79713] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6f3f22a28b]
[runnervmg397c:79713] [11] plumed(+0x134a5)[0x5649de9634a5]
[runnervmg397c:79713] *** End of error message ***
</pre>
{% endraw %}
