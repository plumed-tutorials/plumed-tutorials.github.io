Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[runnervm3jyl0:46924] *** Process received signal ***
[runnervm3jyl0:46924] Signal: Aborted (6)
[runnervm3jyl0:46924] Signal code:  (-6)
[runnervm3jyl0:46924] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2a40845330]
[runnervm3jyl0:46924] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2a4089eb2c]
[runnervm3jyl0:46924] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2a4084527e]
[runnervm3jyl0:46924] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2a408288ff]
[runnervm3jyl0:46924] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2a40ca5ff5]
[runnervm3jyl0:46924] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2a40cbb0da]
[runnervm3jyl0:46924] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2a40ca5a55]
[runnervm3jyl0:46924] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2a40ca5a6f]
[runnervm3jyl0:46924] [ 8] plumed(+0x13209)[0x557018735209]
[runnervm3jyl0:46924] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2a4082a1ca]
[runnervm3jyl0:46924] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2a4082a28b]
[runnervm3jyl0:46924] [11] plumed(+0x134a5)[0x5570187354a5]
[runnervm3jyl0:46924] *** End of error message ***
</pre>
{% endraw %}
