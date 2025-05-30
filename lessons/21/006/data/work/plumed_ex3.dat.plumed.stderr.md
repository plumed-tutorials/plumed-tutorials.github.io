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
[pkrvmf6wy0o8zjz:60030] *** Process received signal ***
[pkrvmf6wy0o8zjz:60030] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60030] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60030] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3845a45330]
[pkrvmf6wy0o8zjz:60030] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3845a9eb2c]
[pkrvmf6wy0o8zjz:60030] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3845a4527e]
[pkrvmf6wy0o8zjz:60030] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3845a288ff]
[pkrvmf6wy0o8zjz:60030] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3845ea5ff5]
[pkrvmf6wy0o8zjz:60030] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3845ebb0da]
[pkrvmf6wy0o8zjz:60030] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3845ea5a55]
[pkrvmf6wy0o8zjz:60030] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3845ea5a6f]
[pkrvmf6wy0o8zjz:60030] [ 8] plumed(+0x13209)[0x55b9f3fae209]
[pkrvmf6wy0o8zjz:60030] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3845a2a1ca]
[pkrvmf6wy0o8zjz:60030] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3845a2a28b]
[pkrvmf6wy0o8zjz:60030] [11] plumed(+0x134a5)[0x55b9f3fae4a5]
[pkrvmf6wy0o8zjz:60030] *** End of error message ***
</pre>
{% endraw %}
