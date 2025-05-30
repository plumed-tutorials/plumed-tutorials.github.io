Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[pkrvmf6wy0o8zjz:61503] *** Process received signal ***
[pkrvmf6wy0o8zjz:61503] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61503] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61503] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5490e45330]
[pkrvmf6wy0o8zjz:61503] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5490e9eb2c]
[pkrvmf6wy0o8zjz:61503] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5490e4527e]
[pkrvmf6wy0o8zjz:61503] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5490e288ff]
[pkrvmf6wy0o8zjz:61503] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f54912a5ff5]
[pkrvmf6wy0o8zjz:61503] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f54912bb0da]
[pkrvmf6wy0o8zjz:61503] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f54912a5a55]
[pkrvmf6wy0o8zjz:61503] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f54912a5a6f]
[pkrvmf6wy0o8zjz:61503] [ 8] plumed(+0x13209)[0x55ef98408209]
[pkrvmf6wy0o8zjz:61503] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5490e2a1ca]
[pkrvmf6wy0o8zjz:61503] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5490e2a28b]
[pkrvmf6wy0o8zjz:61503] [11] plumed(+0x134a5)[0x55ef984084a5]
[pkrvmf6wy0o8zjz:61503] *** End of error message ***
</pre>
{% endraw %}
