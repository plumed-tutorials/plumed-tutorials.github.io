Stderr for source:  contactMatrix.md_working_7.dat   
Download: [zipped raw stdout](contactMatrix.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[fv-az1755-505:05897] *** Process received signal ***
[fv-az1755-505:05897] Signal: Aborted (6)
[fv-az1755-505:05897] Signal code:  (-6)
[fv-az1755-505:05897] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0c5c245330]
[fv-az1755-505:05897] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0c5c29eb2c]
[fv-az1755-505:05897] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0c5c24527e]
[fv-az1755-505:05897] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0c5c2288ff]
[fv-az1755-505:05897] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0c5c6a5ff5]
[fv-az1755-505:05897] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0c5c6bb0da]
[fv-az1755-505:05897] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0c5c6a5a55]
[fv-az1755-505:05897] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0c5c6a5a6f]
[fv-az1755-505:05897] [ 8] plumed(+0x13209)[0x55de446ae209]
[fv-az1755-505:05897] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0c5c22a1ca]
[fv-az1755-505:05897] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0c5c22a28b]
[fv-az1755-505:05897] [11] plumed(+0x134a5)[0x55de446ae4a5]
[fv-az1755-505:05897] *** End of error message ***
</pre>
{% endraw %}
