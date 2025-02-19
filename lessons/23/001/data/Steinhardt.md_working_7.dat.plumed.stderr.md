Stderr for source:  Steinhardt.md_working_7.dat   
Download: [zipped raw stdout](Steinhardt.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 MEAN
Maybe a missing space or a typo?
[fv-az1755-505:06389] *** Process received signal ***
[fv-az1755-505:06389] Signal: Aborted (6)
[fv-az1755-505:06389] Signal code:  (-6)
[fv-az1755-505:06389] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9ac8845330]
[fv-az1755-505:06389] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9ac889eb2c]
[fv-az1755-505:06389] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9ac884527e]
[fv-az1755-505:06389] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9ac88288ff]
[fv-az1755-505:06389] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9ac8ca5ff5]
[fv-az1755-505:06389] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9ac8cbb0da]
[fv-az1755-505:06389] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9ac8ca5a55]
[fv-az1755-505:06389] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9ac8ca5a6f]
[fv-az1755-505:06389] [ 8] plumed(+0x13209)[0x557d4760d209]
[fv-az1755-505:06389] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9ac882a1ca]
[fv-az1755-505:06389] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9ac882a28b]
[fv-az1755-505:06389] [11] plumed(+0x134a5)[0x557d4760d4a5]
[fv-az1755-505:06389] *** End of error message ***
</pre>
{% endraw %}
