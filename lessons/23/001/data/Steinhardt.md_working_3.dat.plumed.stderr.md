Stderr for source:  Steinhardt.md_working_3.dat   
Download: [zipped raw stdout](Steinhardt.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmf6wy0o8zjz:59469] *** Process received signal ***
[pkrvmf6wy0o8zjz:59469] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59469] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59469] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f53b2445330]
[pkrvmf6wy0o8zjz:59469] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f53b249eb2c]
[pkrvmf6wy0o8zjz:59469] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f53b244527e]
[pkrvmf6wy0o8zjz:59469] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f53b24288ff]
[pkrvmf6wy0o8zjz:59469] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f53b28a5ff5]
[pkrvmf6wy0o8zjz:59469] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f53b28bb0da]
[pkrvmf6wy0o8zjz:59469] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f53b28a5a55]
[pkrvmf6wy0o8zjz:59469] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f53b28a5a6f]
[pkrvmf6wy0o8zjz:59469] [ 8] plumed(+0x13209)[0x55aec90be209]
[pkrvmf6wy0o8zjz:59469] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f53b242a1ca]
[pkrvmf6wy0o8zjz:59469] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f53b242a28b]
[pkrvmf6wy0o8zjz:59469] [11] plumed(+0x134a5)[0x55aec90be4a5]
[pkrvmf6wy0o8zjz:59469] *** End of error message ***
</pre>
{% endraw %}
