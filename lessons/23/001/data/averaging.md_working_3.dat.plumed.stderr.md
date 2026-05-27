Stderr for source:  averaging.md_working_3.dat   
Download: [zipped raw stdout](averaging.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1
Maybe a missing space or a typo?
[runnervmg397c:80649] *** Process received signal ***
[runnervmg397c:80649] Signal: Aborted (6)
[runnervmg397c:80649] Signal code:  (-6)
[runnervmg397c:80649] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0402e45330]
[runnervmg397c:80649] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0402e9eb2c]
[runnervmg397c:80649] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0402e4527e]
[runnervmg397c:80649] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0402e288ff]
[runnervmg397c:80649] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f04032a5ff5]
[runnervmg397c:80649] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f04032bb0da]
[runnervmg397c:80649] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f04032a5a55]
[runnervmg397c:80649] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f04032a5a6f]
[runnervmg397c:80649] [ 8] plumed(+0x13209)[0x55a2732e3209]
[runnervmg397c:80649] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0402e2a1ca]
[runnervmg397c:80649] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0402e2a28b]
[runnervmg397c:80649] [11] plumed(+0x134a5)[0x55a2732e34a5]
[runnervmg397c:80649] *** End of error message ***
</pre>
{% endraw %}
