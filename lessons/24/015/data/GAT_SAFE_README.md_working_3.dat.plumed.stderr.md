Stderr for source:  GAT_SAFE_README.md_working_3.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cv1 ATOMS=@mdatoms IMPORT=pycvPersistentData CALCULATE=pydist INIT=pyinit
Maybe a missing space or a typo?
[runnervm3jyl0:46647] *** Process received signal ***
[runnervm3jyl0:46647] Signal: Aborted (6)
[runnervm3jyl0:46647] Signal code:  (-6)
[runnervm3jyl0:46647] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f692ae45330]
[runnervm3jyl0:46647] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f692ae9eb2c]
[runnervm3jyl0:46647] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f692ae4527e]
[runnervm3jyl0:46647] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f692ae288ff]
[runnervm3jyl0:46647] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f692b2a5ff5]
[runnervm3jyl0:46647] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f692b2bb0da]
[runnervm3jyl0:46647] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f692b2a5a55]
[runnervm3jyl0:46647] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f692b2a5a6f]
[runnervm3jyl0:46647] [ 8] plumed(+0x13209)[0x55daaaee2209]
[runnervm3jyl0:46647] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f692ae2a1ca]
[runnervm3jyl0:46647] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f692ae2a28b]
[runnervm3jyl0:46647] [11] plumed(+0x134a5)[0x55daaaee24a5]
[runnervm3jyl0:46647] *** End of error message ***
</pre>
{% endraw %}
