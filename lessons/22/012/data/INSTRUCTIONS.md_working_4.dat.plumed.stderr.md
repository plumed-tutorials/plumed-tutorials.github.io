Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmf6wy0o8zjz:59689] *** Process received signal ***
[pkrvmf6wy0o8zjz:59689] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59689] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59689] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa506245330]
[pkrvmf6wy0o8zjz:59689] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa50629eb2c]
[pkrvmf6wy0o8zjz:59689] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa50624527e]
[pkrvmf6wy0o8zjz:59689] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa5062288ff]
[pkrvmf6wy0o8zjz:59689] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa5066a5ff5]
[pkrvmf6wy0o8zjz:59689] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa5066bb0da]
[pkrvmf6wy0o8zjz:59689] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa5066a5a55]
[pkrvmf6wy0o8zjz:59689] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa5066a5a6f]
[pkrvmf6wy0o8zjz:59689] [ 8] plumed(+0x13209)[0x5557bbdc1209]
[pkrvmf6wy0o8zjz:59689] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa50622a1ca]
[pkrvmf6wy0o8zjz:59689] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa50622a28b]
[pkrvmf6wy0o8zjz:59689] [11] plumed(+0x134a5)[0x5557bbdc14a5]
[pkrvmf6wy0o8zjz:59689] *** End of error message ***
</pre>
{% endraw %}
