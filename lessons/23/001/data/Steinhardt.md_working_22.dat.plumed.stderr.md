Stderr for source:  Steinhardt.md_working_22.dat   
Download: [zipped raw stdout](Steinhardt.md_working_22.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_22.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[runnervm3jyl0:48148] *** Process received signal ***
[runnervm3jyl0:48148] Signal: Aborted (6)
[runnervm3jyl0:48148] Signal code:  (-6)
[runnervm3jyl0:48148] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f81c5045330]
[runnervm3jyl0:48148] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f81c509eb2c]
[runnervm3jyl0:48148] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f81c504527e]
[runnervm3jyl0:48148] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f81c50288ff]
[runnervm3jyl0:48148] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f81c54a5ff5]
[runnervm3jyl0:48148] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f81c54bb0da]
[runnervm3jyl0:48148] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f81c54a5a55]
[runnervm3jyl0:48148] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f81c54a5a6f]
[runnervm3jyl0:48148] [ 8] plumed(+0x13209)[0x558efdff8209]
[runnervm3jyl0:48148] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f81c502a1ca]
[runnervm3jyl0:48148] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f81c502a28b]
[runnervm3jyl0:48148] [11] plumed(+0x134a5)[0x558efdff84a5]
[runnervm3jyl0:48148] *** End of error message ***
</pre>
{% endraw %}
