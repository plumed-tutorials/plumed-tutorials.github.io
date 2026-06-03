Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @37 : keyword ARG is compulsory for this action
[runnervm3jyl0:48679] *** Process received signal ***
[runnervm3jyl0:48679] Signal: Aborted (6)
[runnervm3jyl0:48679] Signal code:  (-6)
[runnervm3jyl0:48679] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5e76845330]
[runnervm3jyl0:48679] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5e7689eb2c]
[runnervm3jyl0:48679] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5e7684527e]
[runnervm3jyl0:48679] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5e768288ff]
[runnervm3jyl0:48679] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5e76ca5ff5]
[runnervm3jyl0:48679] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5e76cbb0da]
[runnervm3jyl0:48679] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5e76ca5a55]
[runnervm3jyl0:48679] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5e76ca5a6f]
[runnervm3jyl0:48679] [ 8] plumed_master(+0x146dd)[0x555984d1f6dd]
[runnervm3jyl0:48679] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5e7682a1ca]
[runnervm3jyl0:48679] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5e7682a28b]
[runnervm3jyl0:48679] [11] plumed_master(+0x15365)[0x555984d20365]
[runnervm3jyl0:48679] *** End of error message ***
</pre>
{% endraw %}
