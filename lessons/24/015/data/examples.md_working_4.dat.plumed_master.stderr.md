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
[runnervm3jyl0:79641] *** Process received signal ***
[runnervm3jyl0:79641] Signal: Aborted (6)
[runnervm3jyl0:79641] Signal code:  (-6)
[runnervm3jyl0:79641] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbebb645330]
[runnervm3jyl0:79641] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbebb69eb2c]
[runnervm3jyl0:79641] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbebb64527e]
[runnervm3jyl0:79641] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbebb6288ff]
[runnervm3jyl0:79641] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbebbaa5ff5]
[runnervm3jyl0:79641] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbebbabb0da]
[runnervm3jyl0:79641] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbebbaa5a55]
[runnervm3jyl0:79641] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbebbaa5a6f]
[runnervm3jyl0:79641] [ 8] plumed_master(+0x146dd)[0x555a80d936dd]
[runnervm3jyl0:79641] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbebb62a1ca]
[runnervm3jyl0:79641] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbebb62a28b]
[runnervm3jyl0:79641] [11] plumed_master(+0x15365)[0x555a80d94365]
[runnervm3jyl0:79641] *** End of error message ***
</pre>
{% endraw %}
