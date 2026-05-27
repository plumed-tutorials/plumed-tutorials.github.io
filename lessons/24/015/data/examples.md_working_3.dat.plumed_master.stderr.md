Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[runnervm3jyl0:79596] *** Process received signal ***
[runnervm3jyl0:79596] Signal: Aborted (6)
[runnervm3jyl0:79596] Signal code:  (-6)
[runnervm3jyl0:79596] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffa52645330]
[runnervm3jyl0:79596] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffa5269eb2c]
[runnervm3jyl0:79596] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffa5264527e]
[runnervm3jyl0:79596] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffa526288ff]
[runnervm3jyl0:79596] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffa52aa5ff5]
[runnervm3jyl0:79596] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffa52abb0da]
[runnervm3jyl0:79596] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffa52aa5a55]
[runnervm3jyl0:79596] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffa52aa5a6f]
[runnervm3jyl0:79596] [ 8] plumed_master(+0x146dd)[0x558f975e26dd]
[runnervm3jyl0:79596] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffa5262a1ca]
[runnervm3jyl0:79596] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffa5262a28b]
[runnervm3jyl0:79596] [11] plumed_master(+0x15365)[0x558f975e3365]
[runnervm3jyl0:79596] *** End of error message ***
</pre>
{% endraw %}
