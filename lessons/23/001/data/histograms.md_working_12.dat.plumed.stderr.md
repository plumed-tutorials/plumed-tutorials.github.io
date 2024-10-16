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
[fv-az1426-552:06316] *** Process received signal ***
[fv-az1426-552:06316] Signal: Aborted (6)
[fv-az1426-552:06316] Signal code:  (-6)
[fv-az1426-552:06316] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4f86642520]
[fv-az1426-552:06316] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4f866969fc]
[fv-az1426-552:06316] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4f86642476]
[fv-az1426-552:06316] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4f866287f3]
[fv-az1426-552:06316] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4f86aa2b9e]
[fv-az1426-552:06316] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4f86aae20c]
[fv-az1426-552:06316] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4f86aae277]
[fv-az1426-552:06316] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4f86aae52b]
[fv-az1426-552:06316] [ 8] plumed(+0x12f48)[0x5579164d5f48]
[fv-az1426-552:06316] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4f86629d90]
[fv-az1426-552:06316] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4f86629e40]
[fv-az1426-552:06316] [11] plumed(+0x131e5)[0x5579164d61e5]
[fv-az1426-552:06316] *** End of error message ***
</pre>
{% endraw %}
