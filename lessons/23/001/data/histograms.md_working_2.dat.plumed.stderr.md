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
[fv-az1020-777:05999] *** Process received signal ***
[fv-az1020-777:05999] Signal: Aborted (6)
[fv-az1020-777:05999] Signal code:  (-6)
[fv-az1020-777:05999] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff7e7642520]
[fv-az1020-777:05999] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff7e76969fc]
[fv-az1020-777:05999] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff7e7642476]
[fv-az1020-777:05999] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff7e76287f3]
[fv-az1020-777:05999] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff7e7aa2b9e]
[fv-az1020-777:05999] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff7e7aae20c]
[fv-az1020-777:05999] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff7e7aae277]
[fv-az1020-777:05999] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff7e7aae52b]
[fv-az1020-777:05999] [ 8] plumed(+0x12f48)[0x562710152f48]
[fv-az1020-777:05999] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff7e7629d90]
[fv-az1020-777:05999] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff7e7629e40]
[fv-az1020-777:05999] [11] plumed(+0x131e5)[0x5627101531e5]
[fv-az1020-777:05999] *** End of error message ***
</pre>
{% endraw %}
