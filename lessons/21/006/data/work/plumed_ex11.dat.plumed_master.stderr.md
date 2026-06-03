Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @73 : keyword ARG is compulsory for this action
[runnervm3jyl0:48037] *** Process received signal ***
[runnervm3jyl0:48037] Signal: Aborted (6)
[runnervm3jyl0:48037] Signal code:  (-6)
[runnervm3jyl0:48037] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f31e1245330]
[runnervm3jyl0:48037] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f31e129eb2c]
[runnervm3jyl0:48037] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f31e124527e]
[runnervm3jyl0:48037] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f31e12288ff]
[runnervm3jyl0:48037] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f31e16a5ff5]
[runnervm3jyl0:48037] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f31e16bb0da]
[runnervm3jyl0:48037] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f31e16a5a55]
[runnervm3jyl0:48037] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f31e16a5a6f]
[runnervm3jyl0:48037] [ 8] plumed_master(+0x146dd)[0x560d452af6dd]
[runnervm3jyl0:48037] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f31e122a1ca]
[runnervm3jyl0:48037] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f31e122a28b]
[runnervm3jyl0:48037] [11] plumed_master(+0x15365)[0x560d452b0365]
[runnervm3jyl0:48037] *** End of error message ***
</pre>
{% endraw %}
