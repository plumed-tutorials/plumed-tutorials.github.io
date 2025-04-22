Stderr for source:  work/plumed_ex10.dat   
Download: [zipped raw stdout](plumed_ex10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[fv-az2211-783:07395] *** Process received signal ***
[fv-az2211-783:07395] Signal: Aborted (6)
[fv-az2211-783:07395] Signal code:  (-6)
[fv-az2211-783:07395] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7ae6845330]
[fv-az2211-783:07395] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7ae689eb2c]
[fv-az2211-783:07395] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7ae684527e]
[fv-az2211-783:07395] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7ae68288ff]
[fv-az2211-783:07395] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7ae6ca5ff5]
[fv-az2211-783:07395] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7ae6cbb0da]
[fv-az2211-783:07395] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7ae6ca5a55]
[fv-az2211-783:07395] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7ae6ca5a6f]
[fv-az2211-783:07395] [ 8] plumed(+0x13209)[0x5568da592209]
[fv-az2211-783:07395] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7ae682a1ca]
[fv-az2211-783:07395] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7ae682a28b]
[fv-az2211-783:07395] [11] plumed(+0x134a5)[0x5568da5924a5]
[fv-az2211-783:07395] *** End of error message ***
</pre>
{% endraw %}
