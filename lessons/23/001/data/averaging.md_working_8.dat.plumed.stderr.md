Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[runnervmg397c:80780] *** Process received signal ***
[runnervmg397c:80780] Signal: Aborted (6)
[runnervmg397c:80780] Signal code:  (-6)
[runnervmg397c:80780] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f919b445330]
[runnervmg397c:80780] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f919b49eb2c]
[runnervmg397c:80780] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f919b44527e]
[runnervmg397c:80780] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f919b4288ff]
[runnervmg397c:80780] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f919b8a5ff5]
[runnervmg397c:80780] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f919b8bb0da]
[runnervmg397c:80780] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f919b8a5a55]
[runnervmg397c:80780] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f919b8a5a6f]
[runnervmg397c:80780] [ 8] plumed(+0x13209)[0x55db00c83209]
[runnervmg397c:80780] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f919b42a1ca]
[runnervmg397c:80780] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f919b42a28b]
[runnervmg397c:80780] [11] plumed(+0x134a5)[0x55db00c834a5]
[runnervmg397c:80780] *** End of error message ***
</pre>
{% endraw %}
