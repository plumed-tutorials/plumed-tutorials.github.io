Stderr for source:  histograms.md_working_12.dat   
Download: [zipped raw stdout](histograms.md_working_12.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_12.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1 VOLUMES=f
Maybe a missing space or a typo?
[fv-az1535-978:71476] *** Process received signal ***
[fv-az1535-978:71476] Signal: Aborted (6)
[fv-az1535-978:71476] Signal code:  (-6)
[fv-az1535-978:71476] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f427d642520]
[fv-az1535-978:71476] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f427d6969fc]
[fv-az1535-978:71476] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f427d642476]
[fv-az1535-978:71476] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f427d6287f3]
[fv-az1535-978:71476] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f427daa2b9e]
[fv-az1535-978:71476] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f427daae20c]
[fv-az1535-978:71476] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f427daae277]
[fv-az1535-978:71476] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f427daae52b]
[fv-az1535-978:71476] [ 8] plumed(+0x12f48)[0x55acd4696f48]
[fv-az1535-978:71476] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f427d629d90]
[fv-az1535-978:71476] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f427d629e40]
[fv-az1535-978:71476] [11] plumed(+0x131e5)[0x55acd46971e5]
[fv-az1535-978:71476] *** End of error message ***
</pre>
{% endraw %}
