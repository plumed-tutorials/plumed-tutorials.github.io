Stderr for source:  contactMatrix.md_working_6.dat   
Download: [zipped raw stdout](contactMatrix.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_6.dat.plumed.stderr.txt.zip) 
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
[fv-az1755-505:05853] *** Process received signal ***
[fv-az1755-505:05853] Signal: Aborted (6)
[fv-az1755-505:05853] Signal code:  (-6)
[fv-az1755-505:05853] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fab17c45330]
[fv-az1755-505:05853] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fab17c9eb2c]
[fv-az1755-505:05853] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fab17c4527e]
[fv-az1755-505:05853] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fab17c288ff]
[fv-az1755-505:05853] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fab180a5ff5]
[fv-az1755-505:05853] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fab180bb0da]
[fv-az1755-505:05853] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fab180a5a55]
[fv-az1755-505:05853] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fab180a5a6f]
[fv-az1755-505:05853] [ 8] plumed(+0x13209)[0x5584fca8a209]
[fv-az1755-505:05853] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fab17c2a1ca]
[fv-az1755-505:05853] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fab17c2a28b]
[fv-az1755-505:05853] [11] plumed(+0x134a5)[0x5584fca8a4a5]
[fv-az1755-505:05853] *** End of error message ***
</pre>
{% endraw %}
