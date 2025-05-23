Stderr for source:  Behler.md_working_4.dat   
Download: [zipped raw stdout](Behler.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:60197] *** Process received signal ***
[pkrvmf6wy0o8zjz:60197] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60197] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60197] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f61dd645330]
[pkrvmf6wy0o8zjz:60197] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f61dd69eb2c]
[pkrvmf6wy0o8zjz:60197] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f61dd64527e]
[pkrvmf6wy0o8zjz:60197] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f61dd6288ff]
[pkrvmf6wy0o8zjz:60197] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f61ddaa5ff5]
[pkrvmf6wy0o8zjz:60197] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f61ddabb0da]
[pkrvmf6wy0o8zjz:60197] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f61ddaa5a55]
[pkrvmf6wy0o8zjz:60197] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f61ddaa5a6f]
[pkrvmf6wy0o8zjz:60197] [ 8] plumed(+0x13209)[0x55644c5c5209]
[pkrvmf6wy0o8zjz:60197] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f61dd62a1ca]
[pkrvmf6wy0o8zjz:60197] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f61dd62a28b]
[pkrvmf6wy0o8zjz:60197] [11] plumed(+0x134a5)[0x55644c5c54a5]
[pkrvmf6wy0o8zjz:60197] *** End of error message ***
</pre>
{% endraw %}
