Stderr for source:  Behler.md_working_2.dat   
Download: [zipped raw stdout](Behler.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmf6wy0o8zjz:60384] *** Process received signal ***
[pkrvmf6wy0o8zjz:60384] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60384] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60384] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f95e1245330]
[pkrvmf6wy0o8zjz:60384] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f95e129eb2c]
[pkrvmf6wy0o8zjz:60384] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f95e124527e]
[pkrvmf6wy0o8zjz:60384] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f95e12288ff]
[pkrvmf6wy0o8zjz:60384] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f95e16a5ff5]
[pkrvmf6wy0o8zjz:60384] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f95e16bb0da]
[pkrvmf6wy0o8zjz:60384] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f95e16a5a55]
[pkrvmf6wy0o8zjz:60384] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f95e16a5a6f]
[pkrvmf6wy0o8zjz:60384] [ 8] plumed(+0x13209)[0x55fbc6770209]
[pkrvmf6wy0o8zjz:60384] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f95e122a1ca]
[pkrvmf6wy0o8zjz:60384] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f95e122a28b]
[pkrvmf6wy0o8zjz:60384] [11] plumed(+0x134a5)[0x55fbc67704a5]
[pkrvmf6wy0o8zjz:60384] *** End of error message ***
</pre>
{% endraw %}
