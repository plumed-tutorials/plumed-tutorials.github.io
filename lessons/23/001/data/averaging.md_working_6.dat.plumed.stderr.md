Stderr for source:  averaging.md_working_6.dat   
Download: [zipped raw stdout](averaging.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight
Maybe a missing space or a typo?
[runnervmg397c:80731] *** Process received signal ***
[runnervmg397c:80731] Signal: Aborted (6)
[runnervmg397c:80731] Signal code:  (-6)
[runnervmg397c:80731] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9b5fa45330]
[runnervmg397c:80731] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9b5fa9eb2c]
[runnervmg397c:80731] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9b5fa4527e]
[runnervmg397c:80731] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9b5fa288ff]
[runnervmg397c:80731] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9b5fea5ff5]
[runnervmg397c:80731] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9b5febb0da]
[runnervmg397c:80731] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9b5fea5a55]
[runnervmg397c:80731] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9b5fea5a6f]
[runnervmg397c:80731] [ 8] plumed(+0x13209)[0x562f44717209]
[runnervmg397c:80731] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9b5fa2a1ca]
[runnervmg397c:80731] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9b5fa2a28b]
[runnervmg397c:80731] [11] plumed(+0x134a5)[0x562f447174a5]
[runnervmg397c:80731] *** End of error message ***
</pre>
{% endraw %}
