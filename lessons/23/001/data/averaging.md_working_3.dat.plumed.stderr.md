Stderr for source:  averaging.md_working_3.dat   
Download: [zipped raw stdout](averaging.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1
Maybe a missing space or a typo?
[fv-az1315-757:07553] *** Process received signal ***
[fv-az1315-757:07553] Signal: Aborted (6)
[fv-az1315-757:07553] Signal code:  (-6)
[fv-az1315-757:07553] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6fd7a45330]
[fv-az1315-757:07553] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6fd7a9eb2c]
[fv-az1315-757:07553] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6fd7a4527e]
[fv-az1315-757:07553] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6fd7a288ff]
[fv-az1315-757:07553] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6fd7ea5ff5]
[fv-az1315-757:07553] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6fd7ebb0da]
[fv-az1315-757:07553] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6fd7ea5a55]
[fv-az1315-757:07553] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6fd7ea5a6f]
[fv-az1315-757:07553] [ 8] plumed(+0x13209)[0x562fb94df209]
[fv-az1315-757:07553] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6fd7a2a1ca]
[fv-az1315-757:07553] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6fd7a2a28b]
[fv-az1315-757:07553] [11] plumed(+0x134a5)[0x562fb94df4a5]
[fv-az1315-757:07553] *** End of error message ***
</pre>
{% endraw %}
