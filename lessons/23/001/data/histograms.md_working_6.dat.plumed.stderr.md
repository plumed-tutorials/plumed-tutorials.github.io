Stderr for source:  histograms.md_working_6.dat   
Download: [zipped raw stdout](histograms.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PAIRENTROPY LABEL=pp GROUP=1-108 MAXR=2.0 GRID_BIN=20 CUTOFF=1.5 BANDWIDTH=0.13
Maybe a missing space or a typo?
[runnervmg397c:81054] *** Process received signal ***
[runnervmg397c:81054] Signal: Aborted (6)
[runnervmg397c:81054] Signal code:  (-6)
[runnervmg397c:81054] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1ad5e45330]
[runnervmg397c:81054] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1ad5e9eb2c]
[runnervmg397c:81054] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1ad5e4527e]
[runnervmg397c:81054] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1ad5e288ff]
[runnervmg397c:81054] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1ad62a5ff5]
[runnervmg397c:81054] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1ad62bb0da]
[runnervmg397c:81054] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1ad62a5a55]
[runnervmg397c:81054] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1ad62a5a6f]
[runnervmg397c:81054] [ 8] plumed(+0x13209)[0x5593df253209]
[runnervmg397c:81054] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1ad5e2a1ca]
[runnervmg397c:81054] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1ad5e2a28b]
[runnervmg397c:81054] [11] plumed(+0x134a5)[0x5593df2534a5]
[runnervmg397c:81054] *** End of error message ***
</pre>
{% endraw %}
