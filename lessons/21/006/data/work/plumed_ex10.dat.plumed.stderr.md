Stderr for source:  work/plumed_ex10.dat   
Download: [zipped raw stdout](plumed_ex10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex10.dat.plumed.stderr.txt.zip) 
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
[runnervmg397c:79708] *** Process received signal ***
[runnervmg397c:79708] Signal: Aborted (6)
[runnervmg397c:79708] Signal code:  (-6)
[runnervmg397c:79708] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0283845330]
[runnervmg397c:79708] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f028389eb2c]
[runnervmg397c:79708] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f028384527e]
[runnervmg397c:79708] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f02838288ff]
[runnervmg397c:79708] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0283ca5ff5]
[runnervmg397c:79708] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0283cbb0da]
[runnervmg397c:79708] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0283ca5a55]
[runnervmg397c:79708] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0283ca5a6f]
[runnervmg397c:79708] [ 8] plumed(+0x13209)[0x56354d2ef209]
[runnervmg397c:79708] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f028382a1ca]
[runnervmg397c:79708] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f028382a28b]
[runnervmg397c:79708] [11] plumed(+0x134a5)[0x56354d2ef4a5]
[runnervmg397c:79708] *** End of error message ***
</pre>
{% endraw %}
