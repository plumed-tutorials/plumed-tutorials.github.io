Stderr for source:  NAVIGATION.md_working_1.dat   
Download: [zipped raw stdout](NAVIGATION.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](NAVIGATION.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'std::runtime_error'
what():  Can not use metatomic action without the corresponding libraries.
Make sure to configure with `--enable-libmetatomic --enable-libtorch` and that the corresponding libraries are found
[runnervm3jyl0:46513] *** Process received signal ***
[runnervm3jyl0:46513] Signal: Aborted (6)
[runnervm3jyl0:46513] Signal code:  (-6)
[runnervm3jyl0:46513] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbc57a45330]
[runnervm3jyl0:46513] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbc57a9eb2c]
[runnervm3jyl0:46513] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbc57a4527e]
[runnervm3jyl0:46513] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbc57a288ff]
[runnervm3jyl0:46513] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbc57ea5ff5]
[runnervm3jyl0:46513] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbc57ebb0da]
[runnervm3jyl0:46513] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbc57ea5a55]
[runnervm3jyl0:46513] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbc57ea5a6f]
[runnervm3jyl0:46513] [ 8] plumed_master(+0x146dd)[0x55fffd2696dd]
[runnervm3jyl0:46513] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbc57a2a1ca]
[runnervm3jyl0:46513] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbc57a2a28b]
[runnervm3jyl0:46513] [11] plumed_master(+0x15365)[0x55fffd26a365]
[runnervm3jyl0:46513] *** End of error message ***
</pre>
{% endraw %}
