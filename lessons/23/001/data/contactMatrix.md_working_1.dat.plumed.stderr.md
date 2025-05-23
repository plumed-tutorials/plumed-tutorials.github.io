Stderr for source:  contactMatrix.md_working_1.dat   
Download: [zipped raw stdout](contactMatrix.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[pkrvmf6wy0o8zjz:58999] *** Process received signal ***
[pkrvmf6wy0o8zjz:58999] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58999] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58999] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc77fa45330]
[pkrvmf6wy0o8zjz:58999] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc77fa9eb2c]
[pkrvmf6wy0o8zjz:58999] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc77fa4527e]
[pkrvmf6wy0o8zjz:58999] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc77fa288ff]
[pkrvmf6wy0o8zjz:58999] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc77fea5ff5]
[pkrvmf6wy0o8zjz:58999] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc77febb0da]
[pkrvmf6wy0o8zjz:58999] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc77fea5a55]
[pkrvmf6wy0o8zjz:58999] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc77fea5a6f]
[pkrvmf6wy0o8zjz:58999] [ 8] plumed(+0x13209)[0x55ee83b98209]
[pkrvmf6wy0o8zjz:58999] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc77fa2a1ca]
[pkrvmf6wy0o8zjz:58999] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc77fa2a28b]
[pkrvmf6wy0o8zjz:58999] [11] plumed(+0x134a5)[0x55ee83b984a5]
[pkrvmf6wy0o8zjz:58999] *** End of error message ***
</pre>
{% endraw %}
