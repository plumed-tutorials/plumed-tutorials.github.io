Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:59181] *** Process received signal ***
[pkrvmf6wy0o8zjz:59181] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59181] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59181] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2fc6845330]
[pkrvmf6wy0o8zjz:59181] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2fc689eb2c]
[pkrvmf6wy0o8zjz:59181] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2fc684527e]
[pkrvmf6wy0o8zjz:59181] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2fc68288ff]
[pkrvmf6wy0o8zjz:59181] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2fc6ca5ff5]
[pkrvmf6wy0o8zjz:59181] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2fc6cbb0da]
[pkrvmf6wy0o8zjz:59181] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2fc6ca5a55]
[pkrvmf6wy0o8zjz:59181] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2fc6ca5a6f]
[pkrvmf6wy0o8zjz:59181] [ 8] plumed(+0x13209)[0x55b598e6e209]
[pkrvmf6wy0o8zjz:59181] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2fc682a1ca]
[pkrvmf6wy0o8zjz:59181] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2fc682a28b]
[pkrvmf6wy0o8zjz:59181] [11] plumed(+0x134a5)[0x55b598e6e4a5]
[pkrvmf6wy0o8zjz:59181] *** End of error message ***
</pre>
{% endraw %}
