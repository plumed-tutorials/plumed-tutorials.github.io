Stderr for source:  histograms.md_working_3.dat   
Download: [zipped raw stdout](histograms.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 HEIGHTS=hA_h METRIC=hA_icov
Maybe a missing space or a typo?
[fv-az1535-978:71269] *** Process received signal ***
[fv-az1535-978:71269] Signal: Aborted (6)
[fv-az1535-978:71269] Signal code:  (-6)
[fv-az1535-978:71269] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f857ae42520]
[fv-az1535-978:71269] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f857ae969fc]
[fv-az1535-978:71269] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f857ae42476]
[fv-az1535-978:71269] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f857ae287f3]
[fv-az1535-978:71269] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f857b2a2b9e]
[fv-az1535-978:71269] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f857b2ae20c]
[fv-az1535-978:71269] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f857b2ae277]
[fv-az1535-978:71269] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f857b2ae52b]
[fv-az1535-978:71269] [ 8] plumed(+0x12f48)[0x563dcd138f48]
[fv-az1535-978:71269] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f857ae29d90]
[fv-az1535-978:71269] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f857ae29e40]
[fv-az1535-978:71269] [11] plumed(+0x131e5)[0x563dcd1391e5]
[fv-az1535-978:71269] *** End of error message ***
</pre>
{% endraw %}
