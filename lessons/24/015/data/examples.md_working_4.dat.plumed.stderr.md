Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[runnervm3jyl0:46831] *** Process received signal ***
[runnervm3jyl0:46831] Signal: Aborted (6)
[runnervm3jyl0:46831] Signal code:  (-6)
[runnervm3jyl0:46831] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f71d3e45330]
[runnervm3jyl0:46831] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f71d3e9eb2c]
[runnervm3jyl0:46831] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f71d3e4527e]
[runnervm3jyl0:46831] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f71d3e288ff]
[runnervm3jyl0:46831] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f71d42a5ff5]
[runnervm3jyl0:46831] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f71d42bb0da]
[runnervm3jyl0:46831] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f71d42a5a55]
[runnervm3jyl0:46831] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f71d42a5a6f]
[runnervm3jyl0:46831] [ 8] plumed(+0x13209)[0x55d4ccd98209]
[runnervm3jyl0:46831] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f71d3e2a1ca]
[runnervm3jyl0:46831] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f71d3e2a28b]
[runnervm3jyl0:46831] [11] plumed(+0x134a5)[0x55d4ccd984a5]
[runnervm3jyl0:46831] *** End of error message ***
</pre>
{% endraw %}
