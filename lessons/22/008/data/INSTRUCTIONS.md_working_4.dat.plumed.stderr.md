Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.4 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[fv-az1279-640:06309] *** Process received signal ***
[fv-az1279-640:06309] Signal: Aborted (6)
[fv-az1279-640:06309] Signal code:  (-6)
[fv-az1279-640:06309] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efc2d045330]
[fv-az1279-640:06309] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efc2d09eb2c]
[fv-az1279-640:06309] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efc2d04527e]
[fv-az1279-640:06309] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efc2d0288ff]
[fv-az1279-640:06309] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efc2d4a5ff5]
[fv-az1279-640:06309] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efc2d4bb0da]
[fv-az1279-640:06309] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efc2d4a5a55]
[fv-az1279-640:06309] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efc2d4a5a6f]
[fv-az1279-640:06309] [ 8] plumed(+0x13209)[0x55bcf69ba209]
[fv-az1279-640:06309] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efc2d02a1ca]
[fv-az1279-640:06309] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efc2d02a28b]
[fv-az1279-640:06309] [11] plumed(+0x134a5)[0x55bcf69ba4a5]
[fv-az1279-640:06309] *** End of error message ***
</pre>
{% endraw %}
