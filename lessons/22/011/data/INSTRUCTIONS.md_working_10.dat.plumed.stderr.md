Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmf6wy0o8zjz:60217] *** Process received signal ***
[pkrvmf6wy0o8zjz:60217] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60217] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60217] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f76c4a45330]
[pkrvmf6wy0o8zjz:60217] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f76c4a9eb2c]
[pkrvmf6wy0o8zjz:60217] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f76c4a4527e]
[pkrvmf6wy0o8zjz:60217] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f76c4a288ff]
[pkrvmf6wy0o8zjz:60217] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f76c4ea5ff5]
[pkrvmf6wy0o8zjz:60217] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f76c4ebb0da]
[pkrvmf6wy0o8zjz:60217] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f76c4ea5a55]
[pkrvmf6wy0o8zjz:60217] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f76c4ea5a6f]
[pkrvmf6wy0o8zjz:60217] [ 8] plumed(+0x13209)[0x5584bdbae209]
[pkrvmf6wy0o8zjz:60217] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f76c4a2a1ca]
[pkrvmf6wy0o8zjz:60217] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f76c4a2a28b]
[pkrvmf6wy0o8zjz:60217] [11] plumed(+0x134a5)[0x5584bdbae4a5]
[pkrvmf6wy0o8zjz:60217] *** End of error message ***
</pre>
{% endraw %}
