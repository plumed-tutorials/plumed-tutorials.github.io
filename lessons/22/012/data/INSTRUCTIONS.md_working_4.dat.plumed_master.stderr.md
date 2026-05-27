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
[runnervm3jyl0:80657] *** Process received signal ***
[runnervm3jyl0:80657] Signal: Aborted (6)
[runnervm3jyl0:80657] Signal code:  (-6)
[runnervm3jyl0:80657] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa6fbe45330]
[runnervm3jyl0:80657] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa6fbe9eb2c]
[runnervm3jyl0:80657] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa6fbe4527e]
[runnervm3jyl0:80657] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa6fbe288ff]
[runnervm3jyl0:80657] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa6fc2a5ff5]
[runnervm3jyl0:80657] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa6fc2bb0da]
[runnervm3jyl0:80657] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa6fc2a5a55]
[runnervm3jyl0:80657] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa6fc2a5a6f]
[runnervm3jyl0:80657] [ 8] plumed_master(+0x146dd)[0x5645db9eb6dd]
[runnervm3jyl0:80657] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa6fbe2a1ca]
[runnervm3jyl0:80657] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa6fbe2a28b]
[runnervm3jyl0:80657] [11] plumed_master(+0x15365)[0x5645db9ec365]
[runnervm3jyl0:80657] *** End of error message ***
</pre>
{% endraw %}
