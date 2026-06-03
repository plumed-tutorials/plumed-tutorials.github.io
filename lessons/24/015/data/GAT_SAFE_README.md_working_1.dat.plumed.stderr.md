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
[runnervm3jyl0:46557] *** Process received signal ***
[runnervm3jyl0:46557] Signal: Aborted (6)
[runnervm3jyl0:46557] Signal code:  (-6)
[runnervm3jyl0:46557] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f49ce245330]
[runnervm3jyl0:46557] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f49ce29eb2c]
[runnervm3jyl0:46557] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f49ce24527e]
[runnervm3jyl0:46557] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f49ce2288ff]
[runnervm3jyl0:46557] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f49ce6a5ff5]
[runnervm3jyl0:46557] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f49ce6bb0da]
[runnervm3jyl0:46557] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f49ce6a5a55]
[runnervm3jyl0:46557] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f49ce6a5a6f]
[runnervm3jyl0:46557] [ 8] plumed(+0x13209)[0x5558a95ce209]
[runnervm3jyl0:46557] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f49ce22a1ca]
[runnervm3jyl0:46557] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f49ce22a28b]
[runnervm3jyl0:46557] [11] plumed(+0x134a5)[0x5558a95ce4a5]
[runnervm3jyl0:46557] *** End of error message ***
</pre>
{% endraw %}
