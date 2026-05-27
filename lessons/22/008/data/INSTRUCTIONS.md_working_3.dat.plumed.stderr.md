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
[runnervm3jyl0:80922] *** Process received signal ***
[runnervm3jyl0:80922] Signal: Aborted (6)
[runnervm3jyl0:80922] Signal code:  (-6)
[runnervm3jyl0:80922] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9722245330]
[runnervm3jyl0:80922] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f972229eb2c]
[runnervm3jyl0:80922] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f972224527e]
[runnervm3jyl0:80922] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f97222288ff]
[runnervm3jyl0:80922] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f97226a5ff5]
[runnervm3jyl0:80922] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f97226bb0da]
[runnervm3jyl0:80922] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f97226a5a55]
[runnervm3jyl0:80922] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f97226a5a6f]
[runnervm3jyl0:80922] [ 8] plumed(+0x13209)[0x55f0ade44209]
[runnervm3jyl0:80922] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f972222a1ca]
[runnervm3jyl0:80922] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f972222a28b]
[runnervm3jyl0:80922] [11] plumed(+0x134a5)[0x55f0ade444a5]
[runnervm3jyl0:80922] *** End of error message ***
</pre>
{% endraw %}
