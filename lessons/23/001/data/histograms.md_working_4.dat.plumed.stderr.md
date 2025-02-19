Stderr for source:  histograms.md_working_4.dat   
Download: [zipped raw stdout](histograms.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=c1 GRID_MIN=0.0 GRID_MAX=12.0 GRID_BIN=120 BANDWIDTH=0.1
Maybe a missing space or a typo?
[fv-az1755-505:07798] *** Process received signal ***
[fv-az1755-505:07798] Signal: Aborted (6)
[fv-az1755-505:07798] Signal code:  (-6)
[fv-az1755-505:07798] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f960e845330]
[fv-az1755-505:07798] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f960e89eb2c]
[fv-az1755-505:07798] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f960e84527e]
[fv-az1755-505:07798] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f960e8288ff]
[fv-az1755-505:07798] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f960eca5ff5]
[fv-az1755-505:07798] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f960ecbb0da]
[fv-az1755-505:07798] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f960eca5a55]
[fv-az1755-505:07798] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f960eca5a6f]
[fv-az1755-505:07798] [ 8] plumed(+0x13209)[0x55ae61796209]
[fv-az1755-505:07798] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f960e82a1ca]
[fv-az1755-505:07798] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f960e82a28b]
[fv-az1755-505:07798] [11] plumed(+0x134a5)[0x55ae617964a5]
[fv-az1755-505:07798] *** End of error message ***
</pre>
{% endraw %}
