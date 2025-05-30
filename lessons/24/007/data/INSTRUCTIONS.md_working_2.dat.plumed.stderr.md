Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[pkrvmf6wy0o8zjz:59303] *** Process received signal ***
[pkrvmf6wy0o8zjz:59303] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59303] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59303] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f20ff845330]
[pkrvmf6wy0o8zjz:59303] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f20ff89eb2c]
[pkrvmf6wy0o8zjz:59303] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f20ff84527e]
[pkrvmf6wy0o8zjz:59303] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f20ff8288ff]
[pkrvmf6wy0o8zjz:59303] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f20ffca5ff5]
[pkrvmf6wy0o8zjz:59303] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f20ffcbb0da]
[pkrvmf6wy0o8zjz:59303] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f20ffca5a55]
[pkrvmf6wy0o8zjz:59303] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f20ffca5a6f]
[pkrvmf6wy0o8zjz:59303] [ 8] plumed(+0x13209)[0x55c03085b209]
[pkrvmf6wy0o8zjz:59303] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f20ff82a1ca]
[pkrvmf6wy0o8zjz:59303] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f20ff82a28b]
[pkrvmf6wy0o8zjz:59303] [11] plumed(+0x134a5)[0x55c03085b4a5]
[pkrvmf6wy0o8zjz:59303] *** End of error message ***
</pre>
{% endraw %}
