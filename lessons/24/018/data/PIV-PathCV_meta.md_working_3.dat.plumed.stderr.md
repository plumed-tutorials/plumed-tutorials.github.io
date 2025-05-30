Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:59165] *** Process received signal ***
[pkrvmf6wy0o8zjz:59165] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59165] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59165] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3918c45330]
[pkrvmf6wy0o8zjz:59165] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3918c9eb2c]
[pkrvmf6wy0o8zjz:59165] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3918c4527e]
[pkrvmf6wy0o8zjz:59165] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3918c288ff]
[pkrvmf6wy0o8zjz:59165] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f39190a5ff5]
[pkrvmf6wy0o8zjz:59165] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f39190bb0da]
[pkrvmf6wy0o8zjz:59165] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f39190a5a55]
[pkrvmf6wy0o8zjz:59165] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f39190a5a6f]
[pkrvmf6wy0o8zjz:59165] [ 8] plumed(+0x13209)[0x562a89bb5209]
[pkrvmf6wy0o8zjz:59165] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3918c2a1ca]
[pkrvmf6wy0o8zjz:59165] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3918c2a28b]
[pkrvmf6wy0o8zjz:59165] [11] plumed(+0x134a5)[0x562a89bb54a5]
[pkrvmf6wy0o8zjz:59165] *** End of error message ***
</pre>
{% endraw %}
