Stderr for source:  RMSD.md_working_6.dat   
Download: [zipped raw stdout](RMSD.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action RMSD with label rmsd : cannot understand the following words from the input line : DISPLACEMENT
[pkrvmf6wy0o8zjz:61761] *** Process received signal ***
[pkrvmf6wy0o8zjz:61761] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61761] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61761] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f311f445330]
[pkrvmf6wy0o8zjz:61761] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f311f49eb2c]
[pkrvmf6wy0o8zjz:61761] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f311f44527e]
[pkrvmf6wy0o8zjz:61761] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f311f4288ff]
[pkrvmf6wy0o8zjz:61761] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f311f8a5ff5]
[pkrvmf6wy0o8zjz:61761] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f311f8bb0da]
[pkrvmf6wy0o8zjz:61761] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f311f8a5a55]
[pkrvmf6wy0o8zjz:61761] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f311f8a5a6f]
[pkrvmf6wy0o8zjz:61761] [ 8] plumed(+0x13209)[0x55be0d020209]
[pkrvmf6wy0o8zjz:61761] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f311f42a1ca]
[pkrvmf6wy0o8zjz:61761] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f311f42a28b]
[pkrvmf6wy0o8zjz:61761] [11] plumed(+0x134a5)[0x55be0d0204a5]
[pkrvmf6wy0o8zjz:61761] *** End of error message ***
</pre>
{% endraw %}
