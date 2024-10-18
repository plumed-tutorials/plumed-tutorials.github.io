Stderr for source:  histograms.md_working_6.dat   
Download: [zipped raw stdout](histograms.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: RDF LABEL=rdf GROUP=1-1000 GRID_BIN=100 MAXR=1.0 BANDWIDTH=0.01
Maybe a missing space or a typo?
[fv-az1535-978:71335] *** Process received signal ***
[fv-az1535-978:71335] Signal: Aborted (6)
[fv-az1535-978:71335] Signal code:  (-6)
[fv-az1535-978:71335] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f537c442520]
[fv-az1535-978:71335] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f537c4969fc]
[fv-az1535-978:71335] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f537c442476]
[fv-az1535-978:71335] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f537c4287f3]
[fv-az1535-978:71335] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f537c8a2b9e]
[fv-az1535-978:71335] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f537c8ae20c]
[fv-az1535-978:71335] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f537c8ae277]
[fv-az1535-978:71335] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f537c8ae52b]
[fv-az1535-978:71335] [ 8] plumed(+0x12f48)[0x562f3930df48]
[fv-az1535-978:71335] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f537c429d90]
[fv-az1535-978:71335] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f537c429e40]
[fv-az1535-978:71335] [11] plumed(+0x131e5)[0x562f3930e1e5]
[fv-az1535-978:71335] *** End of error message ***
</pre>
{% endraw %}
