Stderr for source:  Steinhardt.md_working_9.dat   
Download: [zipped raw stdout](Steinhardt.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 VMEAN
Maybe a missing space or a typo?
[runnervm3jyl0:47739] *** Process received signal ***
[runnervm3jyl0:47739] Signal: Aborted (6)
[runnervm3jyl0:47739] Signal code:  (-6)
[runnervm3jyl0:47739] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6a54645330]
[runnervm3jyl0:47739] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6a5469eb2c]
[runnervm3jyl0:47739] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6a5464527e]
[runnervm3jyl0:47739] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6a546288ff]
[runnervm3jyl0:47739] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6a54aa5ff5]
[runnervm3jyl0:47739] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6a54abb0da]
[runnervm3jyl0:47739] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6a54aa5a55]
[runnervm3jyl0:47739] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6a54aa5a6f]
[runnervm3jyl0:47739] [ 8] plumed(+0x13209)[0x5566b6cf2209]
[runnervm3jyl0:47739] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6a5462a1ca]
[runnervm3jyl0:47739] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6a5462a28b]
[runnervm3jyl0:47739] [11] plumed(+0x134a5)[0x5566b6cf24a5]
[runnervm3jyl0:47739] *** End of error message ***
</pre>
{% endraw %}
