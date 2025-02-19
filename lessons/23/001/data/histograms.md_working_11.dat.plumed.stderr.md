Stderr for source:  histograms.md_working_11.dat   
Download: [zipped raw stdout](histograms.md_working_11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1 HEIGHTS=one
Maybe a missing space or a typo?
[fv-az1755-505:08038] *** Process received signal ***
[fv-az1755-505:08038] Signal: Aborted (6)
[fv-az1755-505:08038] Signal code:  (-6)
[fv-az1755-505:08038] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6bdea45330]
[fv-az1755-505:08038] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6bdea9eb2c]
[fv-az1755-505:08038] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6bdea4527e]
[fv-az1755-505:08038] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6bdea288ff]
[fv-az1755-505:08038] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6bdeea5ff5]
[fv-az1755-505:08038] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6bdeebb0da]
[fv-az1755-505:08038] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6bdeea5a55]
[fv-az1755-505:08038] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6bdeea5a6f]
[fv-az1755-505:08038] [ 8] plumed(+0x13209)[0x5577d6687209]
[fv-az1755-505:08038] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6bdea2a1ca]
[fv-az1755-505:08038] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6bdea2a28b]
[fv-az1755-505:08038] [11] plumed(+0x134a5)[0x5577d66874a5]
[fv-az1755-505:08038] *** End of error message ***
</pre>
{% endraw %}
