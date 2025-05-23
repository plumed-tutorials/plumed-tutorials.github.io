Stderr for source:  Steinhardt.md_working_2.dat   
Download: [zipped raw stdout](Steinhardt.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmf6wy0o8zjz:59438] *** Process received signal ***
[pkrvmf6wy0o8zjz:59438] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59438] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59438] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f783ee45330]
[pkrvmf6wy0o8zjz:59438] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f783ee9eb2c]
[pkrvmf6wy0o8zjz:59438] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f783ee4527e]
[pkrvmf6wy0o8zjz:59438] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f783ee288ff]
[pkrvmf6wy0o8zjz:59438] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f783f2a5ff5]
[pkrvmf6wy0o8zjz:59438] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f783f2bb0da]
[pkrvmf6wy0o8zjz:59438] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f783f2a5a55]
[pkrvmf6wy0o8zjz:59438] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f783f2a5a6f]
[pkrvmf6wy0o8zjz:59438] [ 8] plumed(+0x13209)[0x55b59dce0209]
[pkrvmf6wy0o8zjz:59438] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f783ee2a1ca]
[pkrvmf6wy0o8zjz:59438] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f783ee2a28b]
[pkrvmf6wy0o8zjz:59438] [11] plumed(+0x134a5)[0x55b59dce04a5]
[pkrvmf6wy0o8zjz:59438] *** End of error message ***
</pre>
{% endraw %}
