Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[pkrvmf6wy0o8zjz:60333] *** Process received signal ***
[pkrvmf6wy0o8zjz:60333] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60333] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60333] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fde95245330]
[pkrvmf6wy0o8zjz:60333] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fde9529eb2c]
[pkrvmf6wy0o8zjz:60333] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fde9524527e]
[pkrvmf6wy0o8zjz:60333] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fde952288ff]
[pkrvmf6wy0o8zjz:60333] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fde956a5ff5]
[pkrvmf6wy0o8zjz:60333] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fde956bb0da]
[pkrvmf6wy0o8zjz:60333] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fde956a5a55]
[pkrvmf6wy0o8zjz:60333] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fde956a5a6f]
[pkrvmf6wy0o8zjz:60333] [ 8] plumed(+0x13209)[0x55b0de122209]
[pkrvmf6wy0o8zjz:60333] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fde9522a1ca]
[pkrvmf6wy0o8zjz:60333] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fde9522a28b]
[pkrvmf6wy0o8zjz:60333] [11] plumed(+0x134a5)[0x55b0de1224a5]
[pkrvmf6wy0o8zjz:60333] *** End of error message ***
</pre>
{% endraw %}
