Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[runnervm3jyl0:47344] *** Process received signal ***
[runnervm3jyl0:47344] Signal: Aborted (6)
[runnervm3jyl0:47344] Signal code:  (-6)
[runnervm3jyl0:47344] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1e90645330]
[runnervm3jyl0:47344] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1e9069eb2c]
[runnervm3jyl0:47344] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1e9064527e]
[runnervm3jyl0:47344] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1e906288ff]
[runnervm3jyl0:47344] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1e90aa5ff5]
[runnervm3jyl0:47344] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1e90abb0da]
[runnervm3jyl0:47344] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1e90aa5a55]
[runnervm3jyl0:47344] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1e90aa5a6f]
[runnervm3jyl0:47344] [ 8] plumed_master(+0x146dd)[0x55f483f116dd]
[runnervm3jyl0:47344] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1e9062a1ca]
[runnervm3jyl0:47344] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1e9062a28b]
[runnervm3jyl0:47344] [11] plumed_master(+0x15365)[0x55f483f12365]
[runnervm3jyl0:47344] *** End of error message ***
</pre>
{% endraw %}
