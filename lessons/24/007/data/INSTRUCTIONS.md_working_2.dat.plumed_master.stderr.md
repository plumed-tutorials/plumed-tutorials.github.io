Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[pkrvmf6wy0o8zjz:59393] *** Process received signal ***
[pkrvmf6wy0o8zjz:59393] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59393] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59393] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f20e7445330]
[pkrvmf6wy0o8zjz:59393] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f20e749eb2c]
[pkrvmf6wy0o8zjz:59393] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f20e744527e]
[pkrvmf6wy0o8zjz:59393] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f20e74288ff]
[pkrvmf6wy0o8zjz:59393] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f20e78a5ff5]
[pkrvmf6wy0o8zjz:59393] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f20e78bb0da]
[pkrvmf6wy0o8zjz:59393] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f20e78a5a55]
[pkrvmf6wy0o8zjz:59393] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f20e78a5a6f]
[pkrvmf6wy0o8zjz:59393] [ 8] plumed_master(+0x146dd)[0x55d7b672f6dd]
[pkrvmf6wy0o8zjz:59393] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f20e742a1ca]
[pkrvmf6wy0o8zjz:59393] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f20e742a28b]
[pkrvmf6wy0o8zjz:59393] [11] plumed_master(+0x15365)[0x55d7b6730365]
[pkrvmf6wy0o8zjz:59393] *** End of error message ***
</pre>
{% endraw %}
