Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[runnervm3jyl0:79551] *** Process received signal ***
[runnervm3jyl0:79551] Signal: Aborted (6)
[runnervm3jyl0:79551] Signal code:  (-6)
[runnervm3jyl0:79551] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe9f6e45330]
[runnervm3jyl0:79551] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe9f6e9eb2c]
[runnervm3jyl0:79551] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe9f6e4527e]
[runnervm3jyl0:79551] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe9f6e288ff]
[runnervm3jyl0:79551] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe9f72a5ff5]
[runnervm3jyl0:79551] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe9f72bb0da]
[runnervm3jyl0:79551] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe9f72a5a55]
[runnervm3jyl0:79551] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe9f72a5a6f]
[runnervm3jyl0:79551] [ 8] plumed_master(+0x146dd)[0x55ff970726dd]
[runnervm3jyl0:79551] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe9f6e2a1ca]
[runnervm3jyl0:79551] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe9f6e2a28b]
[runnervm3jyl0:79551] [11] plumed_master(+0x15365)[0x55ff97073365]
[runnervm3jyl0:79551] *** End of error message ***
</pre>
{% endraw %}
