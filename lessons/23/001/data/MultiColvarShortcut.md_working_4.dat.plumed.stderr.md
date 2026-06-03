Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervm3jyl0:47180] *** Process received signal ***
[runnervm3jyl0:47180] Signal: Aborted (6)
[runnervm3jyl0:47180] Signal code:  (-6)
[runnervm3jyl0:47180] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff323245330]
[runnervm3jyl0:47180] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff32329eb2c]
[runnervm3jyl0:47180] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff32324527e]
[runnervm3jyl0:47180] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff3232288ff]
[runnervm3jyl0:47180] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff3236a5ff5]
[runnervm3jyl0:47180] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff3236bb0da]
[runnervm3jyl0:47180] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff3236a5a55]
[runnervm3jyl0:47180] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff3236a5a6f]
[runnervm3jyl0:47180] [ 8] plumed(+0x13209)[0x563c9f1c5209]
[runnervm3jyl0:47180] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff32322a1ca]
[runnervm3jyl0:47180] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff32322a28b]
[runnervm3jyl0:47180] [11] plumed(+0x134a5)[0x563c9f1c54a5]
[runnervm3jyl0:47180] *** End of error message ***
</pre>
{% endraw %}
