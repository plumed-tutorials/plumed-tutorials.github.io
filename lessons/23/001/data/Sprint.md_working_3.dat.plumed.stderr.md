Stderr for source:  Sprint.md_working_3.dat   
Download: [zipped raw stdout](Sprint.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label ss : keyword MATRIX is compulsory for this action
[pkrvmf6wy0o8zjz:59558] *** Process received signal ***
[pkrvmf6wy0o8zjz:59558] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59558] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59558] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6a3ba45330]
[pkrvmf6wy0o8zjz:59558] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6a3ba9eb2c]
[pkrvmf6wy0o8zjz:59558] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6a3ba4527e]
[pkrvmf6wy0o8zjz:59558] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6a3ba288ff]
[pkrvmf6wy0o8zjz:59558] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6a3bea5ff5]
[pkrvmf6wy0o8zjz:59558] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6a3bebb0da]
[pkrvmf6wy0o8zjz:59558] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6a3bea5a55]
[pkrvmf6wy0o8zjz:59558] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6a3bea5a6f]
[pkrvmf6wy0o8zjz:59558] [ 8] plumed(+0x13209)[0x559539bab209]
[pkrvmf6wy0o8zjz:59558] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6a3ba2a1ca]
[pkrvmf6wy0o8zjz:59558] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6a3ba2a28b]
[pkrvmf6wy0o8zjz:59558] [11] plumed(+0x134a5)[0x559539bab4a5]
[pkrvmf6wy0o8zjz:59558] *** End of error message ***
</pre>
{% endraw %}
