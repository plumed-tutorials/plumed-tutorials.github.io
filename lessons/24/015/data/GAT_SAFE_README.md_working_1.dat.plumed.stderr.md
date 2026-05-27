Stderr for source:  GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cvPY ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
Maybe a missing space or a typo?
[runnervm3jyl0:79352] *** Process received signal ***
[runnervm3jyl0:79352] Signal: Aborted (6)
[runnervm3jyl0:79352] Signal code:  (-6)
[runnervm3jyl0:79352] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f12d0445330]
[runnervm3jyl0:79352] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f12d049eb2c]
[runnervm3jyl0:79352] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f12d044527e]
[runnervm3jyl0:79352] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f12d04288ff]
[runnervm3jyl0:79352] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f12d08a5ff5]
[runnervm3jyl0:79352] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f12d08bb0da]
[runnervm3jyl0:79352] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f12d08a5a55]
[runnervm3jyl0:79352] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f12d08a5a6f]
[runnervm3jyl0:79352] [ 8] plumed(+0x13209)[0x563f20c14209]
[runnervm3jyl0:79352] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f12d042a1ca]
[runnervm3jyl0:79352] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f12d042a28b]
[runnervm3jyl0:79352] [11] plumed(+0x134a5)[0x563f20c144a5]
[runnervm3jyl0:79352] *** End of error message ***
</pre>
{% endraw %}
