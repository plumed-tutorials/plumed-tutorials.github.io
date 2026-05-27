Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @23 : keyword ARG is compulsory for this action
[runnervm3jyl0:79926] *** Process received signal ***
[runnervm3jyl0:79926] Signal: Aborted (6)
[runnervm3jyl0:79926] Signal code:  (-6)
[runnervm3jyl0:79926] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7e63c45330]
[runnervm3jyl0:79926] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7e63c9eb2c]
[runnervm3jyl0:79926] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7e63c4527e]
[runnervm3jyl0:79926] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7e63c288ff]
[runnervm3jyl0:79926] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7e640a5ff5]
[runnervm3jyl0:79926] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7e640bb0da]
[runnervm3jyl0:79926] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7e640a5a55]
[runnervm3jyl0:79926] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7e640a5a6f]
[runnervm3jyl0:79926] [ 8] plumed_master(+0x146dd)[0x55f82af2d6dd]
[runnervm3jyl0:79926] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7e63c2a1ca]
[runnervm3jyl0:79926] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7e63c2a28b]
[runnervm3jyl0:79926] [11] plumed_master(+0x15365)[0x55f82af2e365]
[runnervm3jyl0:79926] *** End of error message ***
</pre>
{% endraw %}
