Stderr for source:  input.md_working_2.dat   
Download: [zipped raw stdout](input.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](input.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():
Action "MAZE_OPT_ANNEALING" is not known.
[runnervm3jyl0:46782] *** Process received signal ***
[runnervm3jyl0:46782] Signal: Aborted (6)
[runnervm3jyl0:46782] Signal code:  (-6)
[runnervm3jyl0:46782] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f75fdc45330]
[runnervm3jyl0:46782] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f75fdc9eb2c]
[runnervm3jyl0:46782] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f75fdc4527e]
[runnervm3jyl0:46782] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f75fdc288ff]
[runnervm3jyl0:46782] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f75fe0a5ff5]
[runnervm3jyl0:46782] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f75fe0bb0da]
[runnervm3jyl0:46782] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f75fe0a5a55]
[runnervm3jyl0:46782] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f75fe0a5a6f]
[runnervm3jyl0:46782] [ 8] plumed_master(+0x146dd)[0x564957b146dd]
[runnervm3jyl0:46782] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f75fdc2a1ca]
[runnervm3jyl0:46782] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f75fdc2a28b]
[runnervm3jyl0:46782] [11] plumed_master(+0x15365)[0x564957b15365]
[runnervm3jyl0:46782] *** End of error message ***
</pre>
{% endraw %}
