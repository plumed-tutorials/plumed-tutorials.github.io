Stderr for source:  Path.md_working_2.dat   
Download: [zipped raw stdout](Path.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: LOWEST LABEL=p_mindist ARG=p_data
Maybe a missing space or a typo?
[fv-az1315-757:08570] *** Process received signal ***
[fv-az1315-757:08570] Signal: Aborted (6)
[fv-az1315-757:08570] Signal code:  (-6)
[fv-az1315-757:08570] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1fcb445330]
[fv-az1315-757:08570] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1fcb49eb2c]
[fv-az1315-757:08570] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1fcb44527e]
[fv-az1315-757:08570] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1fcb4288ff]
[fv-az1315-757:08570] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1fcb8a5ff5]
[fv-az1315-757:08570] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1fcb8bb0da]
[fv-az1315-757:08570] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1fcb8a5a55]
[fv-az1315-757:08570] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1fcb8a5a6f]
[fv-az1315-757:08570] [ 8] plumed(+0x13209)[0x564e47777209]
[fv-az1315-757:08570] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1fcb42a1ca]
[fv-az1315-757:08570] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1fcb42a28b]
[fv-az1315-757:08570] [11] plumed(+0x134a5)[0x564e477774a5]
[fv-az1315-757:08570] *** End of error message ***
</pre>
{% endraw %}
