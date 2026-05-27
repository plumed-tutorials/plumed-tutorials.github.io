Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[runnervm3jyl0:79900] *** Process received signal ***
[runnervm3jyl0:79900] Signal: Aborted (6)
[runnervm3jyl0:79900] Signal code:  (-6)
[runnervm3jyl0:79900] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f82a2645330]
[runnervm3jyl0:79900] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f82a269eb2c]
[runnervm3jyl0:79900] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f82a264527e]
[runnervm3jyl0:79900] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f82a26288ff]
[runnervm3jyl0:79900] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f82a2aa5ff5]
[runnervm3jyl0:79900] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f82a2abb0da]
[runnervm3jyl0:79900] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f82a2aa5a55]
[runnervm3jyl0:79900] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f82a2aa5a6f]
[runnervm3jyl0:79900] [ 8] plumed_master(+0x146dd)[0x5582a3f5e6dd]
[runnervm3jyl0:79900] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f82a262a1ca]
[runnervm3jyl0:79900] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f82a262a28b]
[runnervm3jyl0:79900] [11] plumed_master(+0x15365)[0x5582a3f5f365]
[runnervm3jyl0:79900] *** End of error message ***
</pre>
{% endraw %}
