Stderr for source:  NAVIGATION.md_working_1.dat   
Download: [zipped raw stdout](NAVIGATION.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](NAVIGATION.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'std::runtime_error'
what():  Can not use metatomic action without the corresponding libraries.
Make sure to configure with `--enable-libmetatomic --enable-libtorch` and that the corresponding libraries are found
[runnervm3jyl0:78814] *** Process received signal ***
[runnervm3jyl0:78814] Signal: Aborted (6)
[runnervm3jyl0:78814] Signal code:  (-6)
[runnervm3jyl0:78814] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f80f5645330]
[runnervm3jyl0:78814] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f80f569eb2c]
[runnervm3jyl0:78814] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f80f564527e]
[runnervm3jyl0:78814] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f80f56288ff]
[runnervm3jyl0:78814] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f80f5aa5ff5]
[runnervm3jyl0:78814] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f80f5abb0da]
[runnervm3jyl0:78814] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f80f5aa5a55]
[runnervm3jyl0:78814] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f80f5aa5a6f]
[runnervm3jyl0:78814] [ 8] plumed_master(+0x146dd)[0x561050ee06dd]
[runnervm3jyl0:78814] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f80f562a1ca]
[runnervm3jyl0:78814] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f80f562a28b]
[runnervm3jyl0:78814] [11] plumed_master(+0x15365)[0x561050ee1365]
[runnervm3jyl0:78814] *** End of error message ***
</pre>
{% endraw %}
