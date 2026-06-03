Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[runnervm3jyl0:48746] *** Process received signal ***
[runnervm3jyl0:48746] Signal: Aborted (6)
[runnervm3jyl0:48746] Signal code:  (-6)
[runnervm3jyl0:48746] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe20d645330]
[runnervm3jyl0:48746] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe20d69eb2c]
[runnervm3jyl0:48746] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe20d64527e]
[runnervm3jyl0:48746] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe20d6288ff]
[runnervm3jyl0:48746] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe20daa5ff5]
[runnervm3jyl0:48746] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe20dabb0da]
[runnervm3jyl0:48746] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe20daa5a55]
[runnervm3jyl0:48746] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe20daa5a6f]
[runnervm3jyl0:48746] [ 8] plumed(+0x13209)[0x55cd981d6209]
[runnervm3jyl0:48746] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe20d62a1ca]
[runnervm3jyl0:48746] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe20d62a28b]
[runnervm3jyl0:48746] [11] plumed(+0x134a5)[0x55cd981d64a5]
[runnervm3jyl0:48746] *** End of error message ***
</pre>
{% endraw %}
