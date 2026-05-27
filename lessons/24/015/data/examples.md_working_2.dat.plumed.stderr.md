Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[runnervm3jyl0:79535] *** Process received signal ***
[runnervm3jyl0:79535] Signal: Aborted (6)
[runnervm3jyl0:79535] Signal code:  (-6)
[runnervm3jyl0:79535] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fab3a045330]
[runnervm3jyl0:79535] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fab3a09eb2c]
[runnervm3jyl0:79535] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fab3a04527e]
[runnervm3jyl0:79535] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fab3a0288ff]
[runnervm3jyl0:79535] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fab3a4a5ff5]
[runnervm3jyl0:79535] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fab3a4bb0da]
[runnervm3jyl0:79535] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fab3a4a5a55]
[runnervm3jyl0:79535] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fab3a4a5a6f]
[runnervm3jyl0:79535] [ 8] plumed(+0x13209)[0x563df923c209]
[runnervm3jyl0:79535] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fab3a02a1ca]
[runnervm3jyl0:79535] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fab3a02a28b]
[runnervm3jyl0:79535] [11] plumed(+0x134a5)[0x563df923c4a5]
[runnervm3jyl0:79535] *** End of error message ***
</pre>
{% endraw %}
