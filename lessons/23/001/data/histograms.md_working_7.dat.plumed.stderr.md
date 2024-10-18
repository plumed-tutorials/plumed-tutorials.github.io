Stderr for source:  histograms.md_working_7.dat   
Download: [zipped raw stdout](histograms.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PAIRENTROPY LABEL=pp GROUP=1-108 MAXR=2.0 GRID_BIN=20 CUTOFF=1.5 BANDWIDTH=0.13
Maybe a missing space or a typo?
[fv-az1535-978:71357] *** Process received signal ***
[fv-az1535-978:71357] Signal: Aborted (6)
[fv-az1535-978:71357] Signal code:  (-6)
[fv-az1535-978:71357] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fef55c42520]
[fv-az1535-978:71357] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fef55c969fc]
[fv-az1535-978:71357] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fef55c42476]
[fv-az1535-978:71357] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fef55c287f3]
[fv-az1535-978:71357] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fef560a2b9e]
[fv-az1535-978:71357] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fef560ae20c]
[fv-az1535-978:71357] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fef560ae277]
[fv-az1535-978:71357] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fef560ae52b]
[fv-az1535-978:71357] [ 8] plumed(+0x12f48)[0x563d74065f48]
[fv-az1535-978:71357] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fef55c29d90]
[fv-az1535-978:71357] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fef55c29e40]
[fv-az1535-978:71357] [11] plumed(+0x131e5)[0x563d740661e5]
[fv-az1535-978:71357] *** End of error message ***
</pre>
{% endraw %}
