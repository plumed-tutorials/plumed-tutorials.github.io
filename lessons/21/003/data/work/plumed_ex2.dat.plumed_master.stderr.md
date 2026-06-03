Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @27 : keyword ARG is compulsory for this action
[runnervm3jyl0:48391] *** Process received signal ***
[runnervm3jyl0:48391] Signal: Aborted (6)
[runnervm3jyl0:48391] Signal code:  (-6)
[runnervm3jyl0:48391] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd40a045330]
[runnervm3jyl0:48391] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd40a09eb2c]
[runnervm3jyl0:48391] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd40a04527e]
[runnervm3jyl0:48391] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd40a0288ff]
[runnervm3jyl0:48391] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd40a4a5ff5]
[runnervm3jyl0:48391] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd40a4bb0da]
[runnervm3jyl0:48391] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd40a4a5a55]
[runnervm3jyl0:48391] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd40a4a5a6f]
[runnervm3jyl0:48391] [ 8] plumed_master(+0x146dd)[0x558d8fe136dd]
[runnervm3jyl0:48391] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd40a02a1ca]
[runnervm3jyl0:48391] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd40a02a28b]
[runnervm3jyl0:48391] [11] plumed_master(+0x15365)[0x558d8fe14365]
[runnervm3jyl0:48391] *** End of error message ***
</pre>
{% endraw %}
