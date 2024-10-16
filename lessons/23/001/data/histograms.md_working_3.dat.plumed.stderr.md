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
[fv-az1426-552:06110] *** Process received signal ***
[fv-az1426-552:06110] Signal: Aborted (6)
[fv-az1426-552:06110] Signal code:  (-6)
[fv-az1426-552:06110] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f73f9442520]
[fv-az1426-552:06110] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f73f94969fc]
[fv-az1426-552:06110] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f73f9442476]
[fv-az1426-552:06110] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f73f94287f3]
[fv-az1426-552:06110] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f73f98a2b9e]
[fv-az1426-552:06110] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f73f98ae20c]
[fv-az1426-552:06110] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f73f98ae277]
[fv-az1426-552:06110] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f73f98ae52b]
[fv-az1426-552:06110] [ 8] plumed(+0x12f48)[0x55b6aa096f48]
[fv-az1426-552:06110] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f73f9429d90]
[fv-az1426-552:06110] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f73f9429e40]
[fv-az1426-552:06110] [11] plumed(+0x131e5)[0x55b6aa0971e5]
[fv-az1426-552:06110] *** End of error message ***
</pre>
{% endraw %}
