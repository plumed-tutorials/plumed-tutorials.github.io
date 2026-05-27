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
[runnervm3jyl0:79889] *** Process received signal ***
[runnervm3jyl0:79889] Signal: Aborted (6)
[runnervm3jyl0:79889] Signal code:  (-6)
[runnervm3jyl0:79889] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f673a845330]
[runnervm3jyl0:79889] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f673a89eb2c]
[runnervm3jyl0:79889] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f673a84527e]
[runnervm3jyl0:79889] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f673a8288ff]
[runnervm3jyl0:79889] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f673aca5ff5]
[runnervm3jyl0:79889] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f673acbb0da]
[runnervm3jyl0:79889] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f673aca5a55]
[runnervm3jyl0:79889] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f673aca5a6f]
[runnervm3jyl0:79889] [ 8] plumed_master(+0x146dd)[0x55879f8076dd]
[runnervm3jyl0:79889] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f673a82a1ca]
[runnervm3jyl0:79889] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f673a82a28b]
[runnervm3jyl0:79889] [11] plumed_master(+0x15365)[0x55879f808365]
[runnervm3jyl0:79889] *** End of error message ***
</pre>
{% endraw %}
