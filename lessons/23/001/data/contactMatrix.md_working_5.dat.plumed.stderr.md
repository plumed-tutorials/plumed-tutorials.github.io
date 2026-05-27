Stderr for source:  contactMatrix.md_working_5.dat   
Download: [zipped raw stdout](contactMatrix.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[runnervmg397c:79361] *** Process received signal ***
[runnervmg397c:79361] Signal: Aborted (6)
[runnervmg397c:79361] Signal code:  (-6)
[runnervmg397c:79361] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa2e3245330]
[runnervmg397c:79361] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa2e329eb2c]
[runnervmg397c:79361] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa2e324527e]
[runnervmg397c:79361] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa2e32288ff]
[runnervmg397c:79361] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa2e36a5ff5]
[runnervmg397c:79361] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa2e36bb0da]
[runnervmg397c:79361] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa2e36a5a55]
[runnervmg397c:79361] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa2e36a5a6f]
[runnervmg397c:79361] [ 8] plumed(+0x13209)[0x559ec43d9209]
[runnervmg397c:79361] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa2e322a1ca]
[runnervmg397c:79361] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa2e322a28b]
[runnervmg397c:79361] [11] plumed(+0x134a5)[0x559ec43d94a5]
[runnervmg397c:79361] *** End of error message ***
</pre>
{% endraw %}
