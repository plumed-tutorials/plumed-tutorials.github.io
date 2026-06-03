Stderr for source:  Steinhardt.md_working_5.dat   
Download: [zipped raw stdout](Steinhardt.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @1 : action q4 has no component named q4 (hint! the components in this actions are: )
[runnervm3jyl0:47614] *** Process received signal ***
[runnervm3jyl0:47614] Signal: Aborted (6)
[runnervm3jyl0:47614] Signal code:  (-6)
[runnervm3jyl0:47614] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0285c45330]
[runnervm3jyl0:47614] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0285c9eb2c]
[runnervm3jyl0:47614] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0285c4527e]
[runnervm3jyl0:47614] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0285c288ff]
[runnervm3jyl0:47614] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f02860a5ff5]
[runnervm3jyl0:47614] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f02860bb0da]
[runnervm3jyl0:47614] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f02860a5a55]
[runnervm3jyl0:47614] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f02860a5a6f]
[runnervm3jyl0:47614] [ 8] plumed(+0x13209)[0x55e2bf61a209]
[runnervm3jyl0:47614] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0285c2a1ca]
[runnervm3jyl0:47614] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0285c2a28b]
[runnervm3jyl0:47614] [11] plumed(+0x134a5)[0x55e2bf61a4a5]
[runnervm3jyl0:47614] *** End of error message ***
</pre>
{% endraw %}
