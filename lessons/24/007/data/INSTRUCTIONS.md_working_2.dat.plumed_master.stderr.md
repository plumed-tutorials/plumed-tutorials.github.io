Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[runnervm3jyl0:80191] *** Process received signal ***
[runnervm3jyl0:80191] Signal: Aborted (6)
[runnervm3jyl0:80191] Signal code:  (-6)
[runnervm3jyl0:80191] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb57ee45330]
[runnervm3jyl0:80191] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb57ee9eb2c]
[runnervm3jyl0:80191] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb57ee4527e]
[runnervm3jyl0:80191] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb57ee288ff]
[runnervm3jyl0:80191] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb57f2a5ff5]
[runnervm3jyl0:80191] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb57f2bb0da]
[runnervm3jyl0:80191] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb57f2a5a55]
[runnervm3jyl0:80191] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb57f2a5a6f]
[runnervm3jyl0:80191] [ 8] plumed_master(+0x146dd)[0x560f1ea126dd]
[runnervm3jyl0:80191] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb57ee2a1ca]
[runnervm3jyl0:80191] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb57ee2a28b]
[runnervm3jyl0:80191] [11] plumed_master(+0x15365)[0x560f1ea13365]
[runnervm3jyl0:80191] *** End of error message ***
</pre>
{% endraw %}
