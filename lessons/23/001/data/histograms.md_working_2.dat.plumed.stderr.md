Stderr for source:  histograms.md_working_2.dat   
Download: [zipped raw stdout](histograms.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1
Maybe a missing space or a typo?
[runnervmg397c:80930] *** Process received signal ***
[runnervmg397c:80930] Signal: Aborted (6)
[runnervmg397c:80930] Signal code:  (-6)
[runnervmg397c:80930] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6177e45330]
[runnervmg397c:80930] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6177e9eb2c]
[runnervmg397c:80930] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6177e4527e]
[runnervmg397c:80930] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6177e288ff]
[runnervmg397c:80930] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f61782a5ff5]
[runnervmg397c:80930] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f61782bb0da]
[runnervmg397c:80930] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f61782a5a55]
[runnervmg397c:80930] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f61782a5a6f]
[runnervmg397c:80930] [ 8] plumed(+0x13209)[0x5593c2588209]
[runnervmg397c:80930] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6177e2a1ca]
[runnervmg397c:80930] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6177e2a28b]
[runnervmg397c:80930] [11] plumed(+0x134a5)[0x5593c25884a5]
[runnervmg397c:80930] *** End of error message ***
</pre>
{% endraw %}
