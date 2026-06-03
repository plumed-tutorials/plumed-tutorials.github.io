Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[runnervm3jyl0:46940] *** Process received signal ***
[runnervm3jyl0:46940] Signal: Aborted (6)
[runnervm3jyl0:46940] Signal code:  (-6)
[runnervm3jyl0:46940] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f134ec45330]
[runnervm3jyl0:46940] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f134ec9eb2c]
[runnervm3jyl0:46940] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f134ec4527e]
[runnervm3jyl0:46940] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f134ec288ff]
[runnervm3jyl0:46940] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f134f0a5ff5]
[runnervm3jyl0:46940] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f134f0bb0da]
[runnervm3jyl0:46940] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f134f0a5a55]
[runnervm3jyl0:46940] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f134f0a5a6f]
[runnervm3jyl0:46940] [ 8] plumed_master(+0x146dd)[0x56284ff226dd]
[runnervm3jyl0:46940] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f134ec2a1ca]
[runnervm3jyl0:46940] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f134ec2a28b]
[runnervm3jyl0:46940] [11] plumed_master(+0x15365)[0x56284ff23365]
[runnervm3jyl0:46940] *** End of error message ***
</pre>
{% endraw %}
