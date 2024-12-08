Stderr for source:  histograms.md_working_4.dat   
Download: [zipped raw stdout](histograms.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=c1 GRID_MIN=0.0 GRID_MAX=12.0 GRID_BIN=120 BANDWIDTH=0.1
Maybe a missing space or a typo?
[fv-az1020-777:06045] *** Process received signal ***
[fv-az1020-777:06045] Signal: Aborted (6)
[fv-az1020-777:06045] Signal code:  (-6)
[fv-az1020-777:06045] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f91e9e42520]
[fv-az1020-777:06045] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f91e9e969fc]
[fv-az1020-777:06045] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f91e9e42476]
[fv-az1020-777:06045] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f91e9e287f3]
[fv-az1020-777:06045] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f91ea2a2b9e]
[fv-az1020-777:06045] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f91ea2ae20c]
[fv-az1020-777:06045] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f91ea2ae277]
[fv-az1020-777:06045] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f91ea2ae52b]
[fv-az1020-777:06045] [ 8] plumed(+0x12f48)[0x55607f361f48]
[fv-az1020-777:06045] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f91e9e29d90]
[fv-az1020-777:06045] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f91e9e29e40]
[fv-az1020-777:06045] [11] plumed(+0x131e5)[0x55607f3621e5]
[fv-az1020-777:06045] *** End of error message ***
</pre>
{% endraw %}
