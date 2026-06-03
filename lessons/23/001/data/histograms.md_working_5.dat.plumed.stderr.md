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
[runnervm3jyl0:48990] *** Process received signal ***
[runnervm3jyl0:48990] Signal: Aborted (6)
[runnervm3jyl0:48990] Signal code:  (-6)
[runnervm3jyl0:48990] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f13bf045330]
[runnervm3jyl0:48990] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f13bf09eb2c]
[runnervm3jyl0:48990] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f13bf04527e]
[runnervm3jyl0:48990] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f13bf0288ff]
[runnervm3jyl0:48990] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f13bf4a5ff5]
[runnervm3jyl0:48990] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f13bf4bb0da]
[runnervm3jyl0:48990] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f13bf4a5a55]
[runnervm3jyl0:48990] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f13bf4a5a6f]
[runnervm3jyl0:48990] [ 8] plumed(+0x13209)[0x55c35a547209]
[runnervm3jyl0:48990] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f13bf02a1ca]
[runnervm3jyl0:48990] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f13bf02a28b]
[runnervm3jyl0:48990] [11] plumed(+0x134a5)[0x55c35a5474a5]
[runnervm3jyl0:48990] *** End of error message ***
</pre>
{% endraw %}
