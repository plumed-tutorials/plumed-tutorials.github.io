Stderr for source:  histograms.md_working_3.dat   
Download: [zipped raw stdout](histograms.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=c1 GRID_MIN=0.0 GRID_MAX=12.0 GRID_BIN=120 BANDWIDTH=0.1
Maybe a missing space or a typo?
[runnervmg397c:80961] *** Process received signal ***
[runnervmg397c:80961] Signal: Aborted (6)
[runnervmg397c:80961] Signal code:  (-6)
[runnervmg397c:80961] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe533c45330]
[runnervmg397c:80961] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe533c9eb2c]
[runnervmg397c:80961] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe533c4527e]
[runnervmg397c:80961] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe533c288ff]
[runnervmg397c:80961] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe5340a5ff5]
[runnervmg397c:80961] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe5340bb0da]
[runnervmg397c:80961] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe5340a5a55]
[runnervmg397c:80961] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe5340a5a6f]
[runnervmg397c:80961] [ 8] plumed(+0x13209)[0x56482d8bd209]
[runnervmg397c:80961] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe533c2a1ca]
[runnervmg397c:80961] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe533c2a28b]
[runnervmg397c:80961] [11] plumed(+0x134a5)[0x56482d8bd4a5]
[runnervmg397c:80961] *** End of error message ***
</pre>
{% endraw %}
