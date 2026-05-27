Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[runnervmg397c:79739] *** Process received signal ***
[runnervmg397c:79739] Signal: Aborted (6)
[runnervmg397c:79739] Signal code:  (-6)
[runnervmg397c:79739] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2f8cc45330]
[runnervmg397c:79739] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2f8cc9eb2c]
[runnervmg397c:79739] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2f8cc4527e]
[runnervmg397c:79739] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2f8cc288ff]
[runnervmg397c:79739] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2f8d0a5ff5]
[runnervmg397c:79739] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2f8d0bb0da]
[runnervmg397c:79739] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2f8d0a5a55]
[runnervmg397c:79739] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2f8d0a5a6f]
[runnervmg397c:79739] [ 8] plumed(+0x13209)[0x5619d2a99209]
[runnervmg397c:79739] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2f8cc2a1ca]
[runnervmg397c:79739] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2f8cc2a28b]
[runnervmg397c:79739] [11] plumed(+0x134a5)[0x5619d2a994a5]
[runnervmg397c:79739] *** End of error message ***
</pre>
{% endraw %}
