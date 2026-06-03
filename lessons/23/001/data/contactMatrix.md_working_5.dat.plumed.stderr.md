Stderr for source:  contactMatrix.md_working_5.dat   
Download: [zipped raw stdout](contactMatrix.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[runnervm3jyl0:47325] *** Process received signal ***
[runnervm3jyl0:47325] Signal: Aborted (6)
[runnervm3jyl0:47325] Signal code:  (-6)
[runnervm3jyl0:47325] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f43e0845330]
[runnervm3jyl0:47325] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f43e089eb2c]
[runnervm3jyl0:47325] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f43e084527e]
[runnervm3jyl0:47325] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f43e08288ff]
[runnervm3jyl0:47325] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f43e0ca5ff5]
[runnervm3jyl0:47325] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f43e0cbb0da]
[runnervm3jyl0:47325] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f43e0ca5a55]
[runnervm3jyl0:47325] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f43e0ca5a6f]
[runnervm3jyl0:47325] [ 8] plumed(+0x13209)[0x55f859253209]
[runnervm3jyl0:47325] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f43e082a1ca]
[runnervm3jyl0:47325] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f43e082a28b]
[runnervm3jyl0:47325] [11] plumed(+0x134a5)[0x55f8592534a5]
[runnervm3jyl0:47325] *** End of error message ***
</pre>
{% endraw %}
