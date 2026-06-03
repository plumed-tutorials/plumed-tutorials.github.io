Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @18 : keyword ARG is compulsory for this action
[runnervm3jyl0:48527] *** Process received signal ***
[runnervm3jyl0:48527] Signal: Aborted (6)
[runnervm3jyl0:48527] Signal code:  (-6)
[runnervm3jyl0:48527] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f53ff245330]
[runnervm3jyl0:48527] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f53ff29eb2c]
[runnervm3jyl0:48527] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f53ff24527e]
[runnervm3jyl0:48527] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f53ff2288ff]
[runnervm3jyl0:48527] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f53ff6a5ff5]
[runnervm3jyl0:48527] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f53ff6bb0da]
[runnervm3jyl0:48527] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f53ff6a5a55]
[runnervm3jyl0:48527] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f53ff6a5a6f]
[runnervm3jyl0:48527] [ 8] plumed_master(+0x146dd)[0x55b2a06596dd]
[runnervm3jyl0:48527] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f53ff22a1ca]
[runnervm3jyl0:48527] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f53ff22a28b]
[runnervm3jyl0:48527] [11] plumed_master(+0x15365)[0x55b2a065a365]
[runnervm3jyl0:48527] *** End of error message ***
</pre>
{% endraw %}
