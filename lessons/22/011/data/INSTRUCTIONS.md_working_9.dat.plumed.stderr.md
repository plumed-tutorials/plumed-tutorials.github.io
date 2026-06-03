Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[runnervm3jyl0:47328] *** Process received signal ***
[runnervm3jyl0:47328] Signal: Aborted (6)
[runnervm3jyl0:47328] Signal code:  (-6)
[runnervm3jyl0:47328] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fddbbe45330]
[runnervm3jyl0:47328] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fddbbe9eb2c]
[runnervm3jyl0:47328] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fddbbe4527e]
[runnervm3jyl0:47328] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fddbbe288ff]
[runnervm3jyl0:47328] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fddbc2a5ff5]
[runnervm3jyl0:47328] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fddbc2bb0da]
[runnervm3jyl0:47328] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fddbc2a5a55]
[runnervm3jyl0:47328] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fddbc2a5a6f]
[runnervm3jyl0:47328] [ 8] plumed(+0x13209)[0x5601d02c5209]
[runnervm3jyl0:47328] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fddbbe2a1ca]
[runnervm3jyl0:47328] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fddbbe2a28b]
[runnervm3jyl0:47328] [11] plumed(+0x134a5)[0x5601d02c54a5]
[runnervm3jyl0:47328] *** End of error message ***
</pre>
{% endraw %}
