Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[runnervm3jyl0:46849] *** Process received signal ***
[runnervm3jyl0:46849] Signal: Aborted (6)
[runnervm3jyl0:46849] Signal code:  (-6)
[runnervm3jyl0:46849] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd517845330]
[runnervm3jyl0:46849] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd51789eb2c]
[runnervm3jyl0:46849] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd51784527e]
[runnervm3jyl0:46849] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd5178288ff]
[runnervm3jyl0:46849] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd517ca5ff5]
[runnervm3jyl0:46849] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd517cbb0da]
[runnervm3jyl0:46849] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd517ca5a55]
[runnervm3jyl0:46849] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd517ca5a6f]
[runnervm3jyl0:46849] [ 8] plumed_master(+0x146dd)[0x55fe7a52b6dd]
[runnervm3jyl0:46849] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd51782a1ca]
[runnervm3jyl0:46849] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd51782a28b]
[runnervm3jyl0:46849] [11] plumed_master(+0x15365)[0x55fe7a52c365]
[runnervm3jyl0:46849] *** End of error message ***
</pre>
{% endraw %}
