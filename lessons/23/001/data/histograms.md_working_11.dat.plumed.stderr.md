Stderr for source:  histograms.md_working_11.dat   
Download: [zipped raw stdout](histograms.md_working_11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1 HEIGHTS=one
Maybe a missing space or a typo?
[fv-az1426-552:06294] *** Process received signal ***
[fv-az1426-552:06294] Signal: Aborted (6)
[fv-az1426-552:06294] Signal code:  (-6)
[fv-az1426-552:06294] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3f6be42520]
[fv-az1426-552:06294] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3f6be969fc]
[fv-az1426-552:06294] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3f6be42476]
[fv-az1426-552:06294] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3f6be287f3]
[fv-az1426-552:06294] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f3f6c2a2b9e]
[fv-az1426-552:06294] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f3f6c2ae20c]
[fv-az1426-552:06294] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f3f6c2ae277]
[fv-az1426-552:06294] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f3f6c2ae52b]
[fv-az1426-552:06294] [ 8] plumed(+0x12f48)[0x5564edcf9f48]
[fv-az1426-552:06294] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3f6be29d90]
[fv-az1426-552:06294] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3f6be29e40]
[fv-az1426-552:06294] [11] plumed(+0x131e5)[0x5564edcfa1e5]
[fv-az1426-552:06294] *** End of error message ***
</pre>
{% endraw %}
