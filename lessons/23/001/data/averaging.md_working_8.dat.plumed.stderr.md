Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[fv-az1315-757:07688] *** Process received signal ***
[fv-az1315-757:07688] Signal: Aborted (6)
[fv-az1315-757:07688] Signal code:  (-6)
[fv-az1315-757:07688] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9c48645330]
[fv-az1315-757:07688] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9c4869eb2c]
[fv-az1315-757:07688] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9c4864527e]
[fv-az1315-757:07688] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9c486288ff]
[fv-az1315-757:07688] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9c48aa5ff5]
[fv-az1315-757:07688] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9c48abb0da]
[fv-az1315-757:07688] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9c48aa5a55]
[fv-az1315-757:07688] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9c48aa5a6f]
[fv-az1315-757:07688] [ 8] plumed(+0x13209)[0x55c0668f4209]
[fv-az1315-757:07688] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9c4862a1ca]
[fv-az1315-757:07688] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9c4862a28b]
[fv-az1315-757:07688] [11] plumed(+0x134a5)[0x55c0668f44a5]
[fv-az1315-757:07688] *** End of error message ***
</pre>
{% endraw %}
