Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[runnervm3jyl0:47419] *** Process received signal ***
[runnervm3jyl0:47419] Signal: Aborted (6)
[runnervm3jyl0:47419] Signal code:  (-6)
[runnervm3jyl0:47419] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe9b0c45330]
[runnervm3jyl0:47419] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe9b0c9eb2c]
[runnervm3jyl0:47419] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe9b0c4527e]
[runnervm3jyl0:47419] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe9b0c288ff]
[runnervm3jyl0:47419] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe9b10a5ff5]
[runnervm3jyl0:47419] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe9b10bb0da]
[runnervm3jyl0:47419] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe9b10a5a55]
[runnervm3jyl0:47419] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe9b10a5a6f]
[runnervm3jyl0:47419] [ 8] plumed(+0x13209)[0x5650ec488209]
[runnervm3jyl0:47419] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe9b0c2a1ca]
[runnervm3jyl0:47419] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe9b0c2a28b]
[runnervm3jyl0:47419] [11] plumed(+0x134a5)[0x5650ec4884a5]
[runnervm3jyl0:47419] *** End of error message ***
</pre>
{% endraw %}
