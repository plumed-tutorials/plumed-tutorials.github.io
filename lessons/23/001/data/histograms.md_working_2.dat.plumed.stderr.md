Stderr for source:  histograms.md_working_2.dat   
Download: [zipped raw stdout](histograms.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: KDE LABEL=hA_kde ARG=x GRID_MIN=0.0 GRID_MAX=3.0 GRID_BIN=100 BANDWIDTH=0.1
Maybe a missing space or a typo?
[runnervm3jyl0:48897] *** Process received signal ***
[runnervm3jyl0:48897] Signal: Aborted (6)
[runnervm3jyl0:48897] Signal code:  (-6)
[runnervm3jyl0:48897] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f50c0845330]
[runnervm3jyl0:48897] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f50c089eb2c]
[runnervm3jyl0:48897] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f50c084527e]
[runnervm3jyl0:48897] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f50c08288ff]
[runnervm3jyl0:48897] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f50c0ca5ff5]
[runnervm3jyl0:48897] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f50c0cbb0da]
[runnervm3jyl0:48897] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f50c0ca5a55]
[runnervm3jyl0:48897] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f50c0ca5a6f]
[runnervm3jyl0:48897] [ 8] plumed(+0x13209)[0x562bf8a37209]
[runnervm3jyl0:48897] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f50c082a1ca]
[runnervm3jyl0:48897] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f50c082a28b]
[runnervm3jyl0:48897] [11] plumed(+0x134a5)[0x562bf8a374a5]
[runnervm3jyl0:48897] *** End of error message ***
</pre>
{% endraw %}
