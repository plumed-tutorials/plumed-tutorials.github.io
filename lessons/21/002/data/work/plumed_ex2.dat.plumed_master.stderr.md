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
[runnervm3jyl0:81343] *** Process received signal ***
[runnervm3jyl0:81343] Signal: Aborted (6)
[runnervm3jyl0:81343] Signal code:  (-6)
[runnervm3jyl0:81343] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe612445330]
[runnervm3jyl0:81343] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe61249eb2c]
[runnervm3jyl0:81343] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe61244527e]
[runnervm3jyl0:81343] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe6124288ff]
[runnervm3jyl0:81343] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe6128a5ff5]
[runnervm3jyl0:81343] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe6128bb0da]
[runnervm3jyl0:81343] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe6128a5a55]
[runnervm3jyl0:81343] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe6128a5a6f]
[runnervm3jyl0:81343] [ 8] plumed_master(+0x146dd)[0x56090b9436dd]
[runnervm3jyl0:81343] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe61242a1ca]
[runnervm3jyl0:81343] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe61242a28b]
[runnervm3jyl0:81343] [11] plumed_master(+0x15365)[0x56090b944365]
[runnervm3jyl0:81343] *** End of error message ***
</pre>
{% endraw %}
