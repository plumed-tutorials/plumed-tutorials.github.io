Stderr for source:  ./solutions/walker-0/plumed_reweight_newcv.dat   
Download: [zipped raw stdout](plumed_reweight_newcv.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight_newcv.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @23 : keyword ARG is compulsory for this action
[runnervm3jyl0:46866] *** Process received signal ***
[runnervm3jyl0:46866] Signal: Aborted (6)
[runnervm3jyl0:46866] Signal code:  (-6)
[runnervm3jyl0:46866] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7afe045330]
[runnervm3jyl0:46866] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7afe09eb2c]
[runnervm3jyl0:46866] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7afe04527e]
[runnervm3jyl0:46866] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7afe0288ff]
[runnervm3jyl0:46866] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7afe4a5ff5]
[runnervm3jyl0:46866] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7afe4bb0da]
[runnervm3jyl0:46866] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7afe4a5a55]
[runnervm3jyl0:46866] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7afe4a5a6f]
[runnervm3jyl0:46866] [ 8] plumed_master(+0x146dd)[0x55d968ce46dd]
[runnervm3jyl0:46866] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7afe02a1ca]
[runnervm3jyl0:46866] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7afe02a28b]
[runnervm3jyl0:46866] [11] plumed_master(+0x15365)[0x55d968ce5365]
[runnervm3jyl0:46866] *** End of error message ***
</pre>
{% endraw %}
