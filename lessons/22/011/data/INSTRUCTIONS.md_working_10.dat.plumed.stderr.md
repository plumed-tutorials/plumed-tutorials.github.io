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
[pkrvmf6wy0o8zjz:60045] *** Process received signal ***
[pkrvmf6wy0o8zjz:60045] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60045] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60045] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb1a3845330]
[pkrvmf6wy0o8zjz:60045] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb1a389eb2c]
[pkrvmf6wy0o8zjz:60045] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb1a384527e]
[pkrvmf6wy0o8zjz:60045] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb1a38288ff]
[pkrvmf6wy0o8zjz:60045] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb1a3ca5ff5]
[pkrvmf6wy0o8zjz:60045] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb1a3cbb0da]
[pkrvmf6wy0o8zjz:60045] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb1a3ca5a55]
[pkrvmf6wy0o8zjz:60045] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb1a3ca5a6f]
[pkrvmf6wy0o8zjz:60045] [ 8] plumed(+0x13209)[0x560690456209]
[pkrvmf6wy0o8zjz:60045] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb1a382a1ca]
[pkrvmf6wy0o8zjz:60045] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb1a382a28b]
[pkrvmf6wy0o8zjz:60045] [11] plumed(+0x134a5)[0x5606904564a5]
[pkrvmf6wy0o8zjz:60045] *** End of error message ***
</pre>
{% endraw %}
