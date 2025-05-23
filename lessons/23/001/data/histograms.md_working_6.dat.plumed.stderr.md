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
I cannot understand line: RDF LABEL=rdf GROUP=1-1000 GRID_BIN=100 MAXR=1.0 BANDWIDTH=0.01
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60979] *** Process received signal ***
[pkrvmf6wy0o8zjz:60979] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60979] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60979] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd94b245330]
[pkrvmf6wy0o8zjz:60979] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd94b29eb2c]
[pkrvmf6wy0o8zjz:60979] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd94b24527e]
[pkrvmf6wy0o8zjz:60979] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd94b2288ff]
[pkrvmf6wy0o8zjz:60979] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd94b6a5ff5]
[pkrvmf6wy0o8zjz:60979] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd94b6bb0da]
[pkrvmf6wy0o8zjz:60979] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd94b6a5a55]
[pkrvmf6wy0o8zjz:60979] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd94b6a5a6f]
[pkrvmf6wy0o8zjz:60979] [ 8] plumed(+0x13209)[0x5591b61fe209]
[pkrvmf6wy0o8zjz:60979] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd94b22a1ca]
[pkrvmf6wy0o8zjz:60979] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd94b22a28b]
[pkrvmf6wy0o8zjz:60979] [11] plumed(+0x134a5)[0x5591b61fe4a5]
[pkrvmf6wy0o8zjz:60979] *** End of error message ***
</pre>
{% endraw %}
