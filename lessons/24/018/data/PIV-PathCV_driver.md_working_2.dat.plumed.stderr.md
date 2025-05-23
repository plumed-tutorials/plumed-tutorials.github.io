Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:58765] *** Process received signal ***
[pkrvmf6wy0o8zjz:58765] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58765] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58765] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6531245330]
[pkrvmf6wy0o8zjz:58765] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f653129eb2c]
[pkrvmf6wy0o8zjz:58765] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f653124527e]
[pkrvmf6wy0o8zjz:58765] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f65312288ff]
[pkrvmf6wy0o8zjz:58765] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f65316a5ff5]
[pkrvmf6wy0o8zjz:58765] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f65316bb0da]
[pkrvmf6wy0o8zjz:58765] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f65316a5a55]
[pkrvmf6wy0o8zjz:58765] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f65316a5a6f]
[pkrvmf6wy0o8zjz:58765] [ 8] plumed(+0x13209)[0x55a5ed82a209]
[pkrvmf6wy0o8zjz:58765] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f653122a1ca]
[pkrvmf6wy0o8zjz:58765] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f653122a28b]
[pkrvmf6wy0o8zjz:58765] [11] plumed(+0x134a5)[0x55a5ed82a4a5]
[pkrvmf6wy0o8zjz:58765] *** End of error message ***
</pre>
{% endraw %}
