Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[runnervm3jyl0:48019] *** Process received signal ***
[runnervm3jyl0:48019] Signal: Aborted (6)
[runnervm3jyl0:48019] Signal code:  (-6)
[runnervm3jyl0:48019] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4540045330]
[runnervm3jyl0:48019] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f454009eb2c]
[runnervm3jyl0:48019] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f454004527e]
[runnervm3jyl0:48019] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f45400288ff]
[runnervm3jyl0:48019] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f45404a5ff5]
[runnervm3jyl0:48019] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f45404bb0da]
[runnervm3jyl0:48019] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f45404a5a55]
[runnervm3jyl0:48019] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f45404a5a6f]
[runnervm3jyl0:48019] [ 8] plumed_master(+0x146dd)[0x5582e10376dd]
[runnervm3jyl0:48019] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f454002a1ca]
[runnervm3jyl0:48019] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f454002a28b]
[runnervm3jyl0:48019] [11] plumed_master(+0x15365)[0x5582e1038365]
[runnervm3jyl0:48019] *** End of error message ***
</pre>
{% endraw %}
