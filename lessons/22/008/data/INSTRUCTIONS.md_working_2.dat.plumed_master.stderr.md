Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[runnervm3jyl0:80893] *** Process received signal ***
[runnervm3jyl0:80893] Signal: Aborted (6)
[runnervm3jyl0:80893] Signal code:  (-6)
[runnervm3jyl0:80893] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbde8045330]
[runnervm3jyl0:80893] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbde809eb2c]
[runnervm3jyl0:80893] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbde804527e]
[runnervm3jyl0:80893] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbde80288ff]
[runnervm3jyl0:80893] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbde84a5ff5]
[runnervm3jyl0:80893] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbde84bb0da]
[runnervm3jyl0:80893] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbde84a5a55]
[runnervm3jyl0:80893] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbde84a5a6f]
[runnervm3jyl0:80893] [ 8] plumed_master(+0x146dd)[0x560a5575e6dd]
[runnervm3jyl0:80893] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbde802a1ca]
[runnervm3jyl0:80893] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbde802a28b]
[runnervm3jyl0:80893] [11] plumed_master(+0x15365)[0x560a5575f365]
[runnervm3jyl0:80893] *** End of error message ***
</pre>
{% endraw %}
