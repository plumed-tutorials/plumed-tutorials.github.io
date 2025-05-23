Stderr for source:  Tasks.md_working_1.dat   
Download: [zipped raw stdout](Tasks.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:59151] *** Process received signal ***
[pkrvmf6wy0o8zjz:59151] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59151] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59151] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1184445330]
[pkrvmf6wy0o8zjz:59151] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f118449eb2c]
[pkrvmf6wy0o8zjz:59151] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f118444527e]
[pkrvmf6wy0o8zjz:59151] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f11844288ff]
[pkrvmf6wy0o8zjz:59151] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f11848a5ff5]
[pkrvmf6wy0o8zjz:59151] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f11848bb0da]
[pkrvmf6wy0o8zjz:59151] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f11848a5a55]
[pkrvmf6wy0o8zjz:59151] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f11848a5a6f]
[pkrvmf6wy0o8zjz:59151] [ 8] plumed(+0x13209)[0x560829bca209]
[pkrvmf6wy0o8zjz:59151] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f118442a1ca]
[pkrvmf6wy0o8zjz:59151] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f118442a28b]
[pkrvmf6wy0o8zjz:59151] [11] plumed(+0x134a5)[0x560829bca4a5]
[pkrvmf6wy0o8zjz:59151] *** End of error message ***
</pre>
{% endraw %}
