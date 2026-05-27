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
[runnervm3jyl0:79857] *** Process received signal ***
[runnervm3jyl0:79857] Signal: Aborted (6)
[runnervm3jyl0:79857] Signal code:  (-6)
[runnervm3jyl0:79857] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0c60a45330]
[runnervm3jyl0:79857] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0c60a9eb2c]
[runnervm3jyl0:79857] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0c60a4527e]
[runnervm3jyl0:79857] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0c60a288ff]
[runnervm3jyl0:79857] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0c60ea5ff5]
[runnervm3jyl0:79857] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0c60ebb0da]
[runnervm3jyl0:79857] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0c60ea5a55]
[runnervm3jyl0:79857] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0c60ea5a6f]
[runnervm3jyl0:79857] [ 8] plumed_master(+0x146dd)[0x55df6926a6dd]
[runnervm3jyl0:79857] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0c60a2a1ca]
[runnervm3jyl0:79857] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0c60a2a28b]
[runnervm3jyl0:79857] [11] plumed_master(+0x15365)[0x55df6926b365]
[runnervm3jyl0:79857] *** End of error message ***
</pre>
{% endraw %}
