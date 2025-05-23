Stderr for source:  Sprint.md_working_1.dat   
Download: [zipped raw stdout](Sprint.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label s1 : keyword MATRIX is compulsory for this action
[pkrvmf6wy0o8zjz:59306] *** Process received signal ***
[pkrvmf6wy0o8zjz:59306] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59306] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59306] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9363445330]
[pkrvmf6wy0o8zjz:59306] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f936349eb2c]
[pkrvmf6wy0o8zjz:59306] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f936344527e]
[pkrvmf6wy0o8zjz:59306] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f93634288ff]
[pkrvmf6wy0o8zjz:59306] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f93638a5ff5]
[pkrvmf6wy0o8zjz:59306] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f93638bb0da]
[pkrvmf6wy0o8zjz:59306] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f93638a5a55]
[pkrvmf6wy0o8zjz:59306] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f93638a5a6f]
[pkrvmf6wy0o8zjz:59306] [ 8] plumed(+0x13209)[0x55db8a2b9209]
[pkrvmf6wy0o8zjz:59306] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f936342a1ca]
[pkrvmf6wy0o8zjz:59306] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f936342a28b]
[pkrvmf6wy0o8zjz:59306] [11] plumed(+0x134a5)[0x55db8a2b94a5]
[pkrvmf6wy0o8zjz:59306] *** End of error message ***
</pre>
{% endraw %}
