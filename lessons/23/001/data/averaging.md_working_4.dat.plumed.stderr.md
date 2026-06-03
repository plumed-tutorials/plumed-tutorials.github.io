Stderr for source:  averaging.md_working_4.dat   
Download: [zipped raw stdout](averaging.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1 CLEAR=100
Maybe a missing space or a typo?
[runnervm3jyl0:48644] *** Process received signal ***
[runnervm3jyl0:48644] Signal: Aborted (6)
[runnervm3jyl0:48644] Signal code:  (-6)
[runnervm3jyl0:48644] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f39e5245330]
[runnervm3jyl0:48644] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f39e529eb2c]
[runnervm3jyl0:48644] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f39e524527e]
[runnervm3jyl0:48644] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f39e52288ff]
[runnervm3jyl0:48644] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f39e56a5ff5]
[runnervm3jyl0:48644] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f39e56bb0da]
[runnervm3jyl0:48644] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f39e56a5a55]
[runnervm3jyl0:48644] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f39e56a5a6f]
[runnervm3jyl0:48644] [ 8] plumed(+0x13209)[0x5615838ea209]
[runnervm3jyl0:48644] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f39e522a1ca]
[runnervm3jyl0:48644] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f39e522a28b]
[runnervm3jyl0:48644] [11] plumed(+0x134a5)[0x5615838ea4a5]
[runnervm3jyl0:48644] *** End of error message ***
</pre>
{% endraw %}
