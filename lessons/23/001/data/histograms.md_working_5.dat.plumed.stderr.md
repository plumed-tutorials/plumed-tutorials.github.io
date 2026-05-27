Stderr for source:  histograms.md_working_5.dat   
Download: [zipped raw stdout](histograms.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: RDF LABEL=rdf GROUP=1-1000 GRID_BIN=100 MAXR=1.0 BANDWIDTH=0.01
Maybe a missing space or a typo?
[runnervmg397c:81023] *** Process received signal ***
[runnervmg397c:81023] Signal: Aborted (6)
[runnervmg397c:81023] Signal code:  (-6)
[runnervmg397c:81023] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa717445330]
[runnervmg397c:81023] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa71749eb2c]
[runnervmg397c:81023] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa71744527e]
[runnervmg397c:81023] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa7174288ff]
[runnervmg397c:81023] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa7178a5ff5]
[runnervmg397c:81023] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa7178bb0da]
[runnervmg397c:81023] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa7178a5a55]
[runnervmg397c:81023] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa7178a5a6f]
[runnervmg397c:81023] [ 8] plumed(+0x13209)[0x55c2e824a209]
[runnervmg397c:81023] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa71742a1ca]
[runnervmg397c:81023] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa71742a28b]
[runnervmg397c:81023] [11] plumed(+0x134a5)[0x55c2e824a4a5]
[runnervmg397c:81023] *** End of error message ***
</pre>
{% endraw %}
