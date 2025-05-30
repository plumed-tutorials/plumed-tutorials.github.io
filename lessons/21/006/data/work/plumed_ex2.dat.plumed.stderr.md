Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PCA with label pca : action cc has no component named cc (hint! the components in this actions are: )
[pkrvmf6wy0o8zjz:59999] *** Process received signal ***
[pkrvmf6wy0o8zjz:59999] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59999] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59999] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f281ee45330]
[pkrvmf6wy0o8zjz:59999] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f281ee9eb2c]
[pkrvmf6wy0o8zjz:59999] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f281ee4527e]
[pkrvmf6wy0o8zjz:59999] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f281ee288ff]
[pkrvmf6wy0o8zjz:59999] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f281f2a5ff5]
[pkrvmf6wy0o8zjz:59999] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f281f2bb0da]
[pkrvmf6wy0o8zjz:59999] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f281f2a5a55]
[pkrvmf6wy0o8zjz:59999] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f281f2a5a6f]
[pkrvmf6wy0o8zjz:59999] [ 8] plumed(+0x13209)[0x55d0d7b5d209]
[pkrvmf6wy0o8zjz:59999] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f281ee2a1ca]
[pkrvmf6wy0o8zjz:59999] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f281ee2a28b]
[pkrvmf6wy0o8zjz:59999] [11] plumed(+0x134a5)[0x55d0d7b5d4a5]
[pkrvmf6wy0o8zjz:59999] *** End of error message ***
</pre>
{% endraw %}
