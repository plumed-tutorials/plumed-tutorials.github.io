Stderr for source:  Steinhardt.md_working_17.dat   
Download: [zipped raw stdout](Steinhardt.md_working_17.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_17.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmf6wy0o8zjz:59910] *** Process received signal ***
[pkrvmf6wy0o8zjz:59910] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59910] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59910] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0afe245330]
[pkrvmf6wy0o8zjz:59910] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0afe29eb2c]
[pkrvmf6wy0o8zjz:59910] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0afe24527e]
[pkrvmf6wy0o8zjz:59910] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0afe2288ff]
[pkrvmf6wy0o8zjz:59910] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0afe6a5ff5]
[pkrvmf6wy0o8zjz:59910] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0afe6bb0da]
[pkrvmf6wy0o8zjz:59910] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0afe6a5a55]
[pkrvmf6wy0o8zjz:59910] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0afe6a5a6f]
[pkrvmf6wy0o8zjz:59910] [ 8] plumed(+0x13209)[0x556f74f47209]
[pkrvmf6wy0o8zjz:59910] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0afe22a1ca]
[pkrvmf6wy0o8zjz:59910] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0afe22a28b]
[pkrvmf6wy0o8zjz:59910] [11] plumed(+0x134a5)[0x556f74f474a5]
[pkrvmf6wy0o8zjz:59910] *** End of error message ***
</pre>
{% endraw %}
