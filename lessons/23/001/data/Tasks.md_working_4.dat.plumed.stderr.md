Stderr for source:  Tasks.md_working_4.dat   
Download: [zipped raw stdout](Tasks.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones SIZE=100
Maybe a missing space or a typo?
[fv-az1315-757:06170] *** Process received signal ***
[fv-az1315-757:06170] Signal: Aborted (6)
[fv-az1315-757:06170] Signal code:  (-6)
[fv-az1315-757:06170] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f495c645330]
[fv-az1315-757:06170] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f495c69eb2c]
[fv-az1315-757:06170] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f495c64527e]
[fv-az1315-757:06170] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f495c6288ff]
[fv-az1315-757:06170] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f495caa5ff5]
[fv-az1315-757:06170] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f495cabb0da]
[fv-az1315-757:06170] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f495caa5a55]
[fv-az1315-757:06170] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f495caa5a6f]
[fv-az1315-757:06170] [ 8] plumed(+0x13209)[0x55e44e9b0209]
[fv-az1315-757:06170] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f495c62a1ca]
[fv-az1315-757:06170] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f495c62a28b]
[fv-az1315-757:06170] [11] plumed(+0x134a5)[0x55e44e9b04a5]
[fv-az1315-757:06170] *** End of error message ***
</pre>
{% endraw %}
