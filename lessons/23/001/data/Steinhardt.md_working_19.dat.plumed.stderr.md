Stderr for source:  Steinhardt.md_working_19.dat   
Download: [zipped raw stdout](Steinhardt.md_working_19.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_19.dat.plumed.stderr.txt.zip) 
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
[runnervm3jyl0:48054] *** Process received signal ***
[runnervm3jyl0:48054] Signal: Aborted (6)
[runnervm3jyl0:48054] Signal code:  (-6)
[runnervm3jyl0:48054] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4ad9645330]
[runnervm3jyl0:48054] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4ad969eb2c]
[runnervm3jyl0:48054] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4ad964527e]
[runnervm3jyl0:48054] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4ad96288ff]
[runnervm3jyl0:48054] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4ad9aa5ff5]
[runnervm3jyl0:48054] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4ad9abb0da]
[runnervm3jyl0:48054] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4ad9aa5a55]
[runnervm3jyl0:48054] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4ad9aa5a6f]
[runnervm3jyl0:48054] [ 8] plumed(+0x13209)[0x55741b00e209]
[runnervm3jyl0:48054] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4ad962a1ca]
[runnervm3jyl0:48054] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4ad962a28b]
[runnervm3jyl0:48054] [11] plumed(+0x134a5)[0x55741b00e4a5]
[runnervm3jyl0:48054] *** End of error message ***
</pre>
{% endraw %}
