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
[runnervm3jyl0:48326] *** Process received signal ***
[runnervm3jyl0:48326] Signal: Aborted (6)
[runnervm3jyl0:48326] Signal code:  (-6)
[runnervm3jyl0:48326] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe1fec45330]
[runnervm3jyl0:48326] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe1fec9eb2c]
[runnervm3jyl0:48326] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe1fec4527e]
[runnervm3jyl0:48326] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe1fec288ff]
[runnervm3jyl0:48326] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe1ff0a5ff5]
[runnervm3jyl0:48326] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe1ff0bb0da]
[runnervm3jyl0:48326] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe1ff0a5a55]
[runnervm3jyl0:48326] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe1ff0a5a6f]
[runnervm3jyl0:48326] [ 8] plumed(+0x13209)[0x5601637e3209]
[runnervm3jyl0:48326] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe1fec2a1ca]
[runnervm3jyl0:48326] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe1fec2a28b]
[runnervm3jyl0:48326] [11] plumed(+0x134a5)[0x5601637e34a5]
[runnervm3jyl0:48326] *** End of error message ***
</pre>
{% endraw %}
