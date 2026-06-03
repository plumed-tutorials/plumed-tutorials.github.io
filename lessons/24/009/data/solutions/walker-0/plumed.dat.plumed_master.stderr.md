Stderr for source:  ./solutions/walker-0/plumed.dat   
Download: [zipped raw stdout](plumed.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action HBOND_MATRIX with label hbmat1 : cannot understand the following words from the input line : SUM
[runnervm3jyl0:46791] *** Process received signal ***
[runnervm3jyl0:46791] Signal: Aborted (6)
[runnervm3jyl0:46791] Signal code:  (-6)
[runnervm3jyl0:46791] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd1ec045330]
[runnervm3jyl0:46791] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd1ec09eb2c]
[runnervm3jyl0:46791] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd1ec04527e]
[runnervm3jyl0:46791] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd1ec0288ff]
[runnervm3jyl0:46791] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd1ec4a5ff5]
[runnervm3jyl0:46791] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd1ec4bb0da]
[runnervm3jyl0:46791] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd1ec4a5a55]
[runnervm3jyl0:46791] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd1ec4a5a6f]
[runnervm3jyl0:46791] [ 8] plumed_master(+0x146dd)[0x562ce04056dd]
[runnervm3jyl0:46791] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd1ec02a1ca]
[runnervm3jyl0:46791] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd1ec02a28b]
[runnervm3jyl0:46791] [11] plumed_master(+0x15365)[0x562ce0406365]
[runnervm3jyl0:46791] *** End of error message ***
</pre>
{% endraw %}
