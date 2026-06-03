Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label @s9 : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[runnervm3jyl0:48107] *** Process received signal ***
[runnervm3jyl0:48107] Signal: Aborted (6)
[runnervm3jyl0:48107] Signal code:  (-6)
[runnervm3jyl0:48107] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffa1c845330]
[runnervm3jyl0:48107] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffa1c89eb2c]
[runnervm3jyl0:48107] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffa1c84527e]
[runnervm3jyl0:48107] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffa1c8288ff]
[runnervm3jyl0:48107] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffa1cca5ff5]
[runnervm3jyl0:48107] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffa1ccbb0da]
[runnervm3jyl0:48107] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffa1cca5a55]
[runnervm3jyl0:48107] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffa1cca5a6f]
[runnervm3jyl0:48107] [ 8] plumed_master(+0x146dd)[0x55aa0bdfe6dd]
[runnervm3jyl0:48107] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffa1c82a1ca]
[runnervm3jyl0:48107] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffa1c82a28b]
[runnervm3jyl0:48107] [11] plumed_master(+0x15365)[0x55aa0bdff365]
[runnervm3jyl0:48107] *** End of error message ***
</pre>
{% endraw %}
