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
[runnervm3jyl0:46741] *** Process received signal ***
[runnervm3jyl0:46741] Signal: Aborted (6)
[runnervm3jyl0:46741] Signal code:  (-6)
[runnervm3jyl0:46741] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7b1a245330]
[runnervm3jyl0:46741] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7b1a29eb2c]
[runnervm3jyl0:46741] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7b1a24527e]
[runnervm3jyl0:46741] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7b1a2288ff]
[runnervm3jyl0:46741] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7b1a6a5ff5]
[runnervm3jyl0:46741] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7b1a6bb0da]
[runnervm3jyl0:46741] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7b1a6a5a55]
[runnervm3jyl0:46741] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7b1a6a5a6f]
[runnervm3jyl0:46741] [ 8] plumed(+0x13209)[0x55fa8775c209]
[runnervm3jyl0:46741] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7b1a22a1ca]
[runnervm3jyl0:46741] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7b1a22a28b]
[runnervm3jyl0:46741] [11] plumed(+0x134a5)[0x55fa8775c4a5]
[runnervm3jyl0:46741] *** End of error message ***
</pre>
{% endraw %}
