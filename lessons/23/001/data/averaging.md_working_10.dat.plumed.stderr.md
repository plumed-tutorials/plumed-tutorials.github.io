Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[runnervmg397c:80861] *** Process received signal ***
[runnervmg397c:80861] Signal: Aborted (6)
[runnervmg397c:80861] Signal code:  (-6)
[runnervmg397c:80861] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb91f245330]
[runnervmg397c:80861] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb91f29eb2c]
[runnervmg397c:80861] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb91f24527e]
[runnervmg397c:80861] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb91f2288ff]
[runnervmg397c:80861] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb91f6a5ff5]
[runnervmg397c:80861] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb91f6bb0da]
[runnervmg397c:80861] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb91f6a5a55]
[runnervmg397c:80861] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb91f6a5a6f]
[runnervmg397c:80861] [ 8] plumed(+0x13209)[0x55a4f1a8a209]
[runnervmg397c:80861] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb91f22a1ca]
[runnervmg397c:80861] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb91f22a28b]
[runnervmg397c:80861] [11] plumed(+0x134a5)[0x55a4f1a8a4a5]
[runnervmg397c:80861] *** End of error message ***
</pre>
{% endraw %}
