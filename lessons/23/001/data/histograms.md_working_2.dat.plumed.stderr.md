Stderr for source:  histograms.md_working_2.dat   
Download: [zipped raw stdout](histograms.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1
Maybe a missing space or a typo?
[fv-az1426-552:06086] *** Process received signal ***
[fv-az1426-552:06086] Signal: Aborted (6)
[fv-az1426-552:06086] Signal code:  (-6)
[fv-az1426-552:06086] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3fb3442520]
[fv-az1426-552:06086] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3fb34969fc]
[fv-az1426-552:06086] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3fb3442476]
[fv-az1426-552:06086] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3fb34287f3]
[fv-az1426-552:06086] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f3fb38a2b9e]
[fv-az1426-552:06086] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f3fb38ae20c]
[fv-az1426-552:06086] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f3fb38ae277]
[fv-az1426-552:06086] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f3fb38ae52b]
[fv-az1426-552:06086] [ 8] plumed(+0x12f48)[0x561e4eaeaf48]
[fv-az1426-552:06086] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3fb3429d90]
[fv-az1426-552:06086] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3fb3429e40]
[fv-az1426-552:06086] [11] plumed(+0x131e5)[0x561e4eaeb1e5]
[fv-az1426-552:06086] *** End of error message ***
</pre>
{% endraw %}
