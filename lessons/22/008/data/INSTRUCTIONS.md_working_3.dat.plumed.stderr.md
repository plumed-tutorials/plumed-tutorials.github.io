Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.5 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[fv-az1279-640:06264] *** Process received signal ***
[fv-az1279-640:06264] Signal: Aborted (6)
[fv-az1279-640:06264] Signal code:  (-6)
[fv-az1279-640:06264] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd40b245330]
[fv-az1279-640:06264] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd40b29eb2c]
[fv-az1279-640:06264] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd40b24527e]
[fv-az1279-640:06264] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd40b2288ff]
[fv-az1279-640:06264] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd40b6a5ff5]
[fv-az1279-640:06264] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd40b6bb0da]
[fv-az1279-640:06264] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd40b6a5a55]
[fv-az1279-640:06264] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd40b6a5a6f]
[fv-az1279-640:06264] [ 8] plumed(+0x13209)[0x55e889c5a209]
[fv-az1279-640:06264] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd40b22a1ca]
[fv-az1279-640:06264] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd40b22a28b]
[fv-az1279-640:06264] [11] plumed(+0x134a5)[0x55e889c5a4a5]
[fv-az1279-640:06264] *** End of error message ***
</pre>
{% endraw %}
