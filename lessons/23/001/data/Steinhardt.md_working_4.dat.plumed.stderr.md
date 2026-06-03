Stderr for source:  Steinhardt.md_working_4.dat   
Download: [zipped raw stdout](Steinhardt.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIESA=1 SPECIESB=2-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[runnervm3jyl0:47583] *** Process received signal ***
[runnervm3jyl0:47583] Signal: Aborted (6)
[runnervm3jyl0:47583] Signal code:  (-6)
[runnervm3jyl0:47583] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5d36845330]
[runnervm3jyl0:47583] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5d3689eb2c]
[runnervm3jyl0:47583] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5d3684527e]
[runnervm3jyl0:47583] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5d368288ff]
[runnervm3jyl0:47583] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5d36ca5ff5]
[runnervm3jyl0:47583] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5d36cbb0da]
[runnervm3jyl0:47583] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5d36ca5a55]
[runnervm3jyl0:47583] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5d36ca5a6f]
[runnervm3jyl0:47583] [ 8] plumed(+0x13209)[0x56391da8d209]
[runnervm3jyl0:47583] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5d3682a1ca]
[runnervm3jyl0:47583] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5d3682a28b]
[runnervm3jyl0:47583] [11] plumed(+0x134a5)[0x56391da8d4a5]
[runnervm3jyl0:47583] *** End of error message ***
</pre>
{% endraw %}
