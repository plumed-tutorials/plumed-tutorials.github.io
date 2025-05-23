Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[pkrvmf6wy0o8zjz:59688] *** Process received signal ***
[pkrvmf6wy0o8zjz:59688] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59688] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59688] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3cd4a45330]
[pkrvmf6wy0o8zjz:59688] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3cd4a9eb2c]
[pkrvmf6wy0o8zjz:59688] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3cd4a4527e]
[pkrvmf6wy0o8zjz:59688] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3cd4a288ff]
[pkrvmf6wy0o8zjz:59688] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3cd4ea5ff5]
[pkrvmf6wy0o8zjz:59688] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3cd4ebb0da]
[pkrvmf6wy0o8zjz:59688] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3cd4ea5a55]
[pkrvmf6wy0o8zjz:59688] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3cd4ea5a6f]
[pkrvmf6wy0o8zjz:59688] [ 8] plumed(+0x13209)[0x55697d1a6209]
[pkrvmf6wy0o8zjz:59688] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3cd4a2a1ca]
[pkrvmf6wy0o8zjz:59688] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3cd4a2a28b]
[pkrvmf6wy0o8zjz:59688] [11] plumed(+0x134a5)[0x55697d1a64a5]
[pkrvmf6wy0o8zjz:59688] *** End of error message ***
</pre>
{% endraw %}
