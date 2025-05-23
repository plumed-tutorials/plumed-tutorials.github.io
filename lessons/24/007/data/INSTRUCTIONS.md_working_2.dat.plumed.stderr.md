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
[pkrvmf6wy0o8zjz:59377] *** Process received signal ***
[pkrvmf6wy0o8zjz:59377] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59377] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59377] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6408845330]
[pkrvmf6wy0o8zjz:59377] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f640889eb2c]
[pkrvmf6wy0o8zjz:59377] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f640884527e]
[pkrvmf6wy0o8zjz:59377] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f64088288ff]
[pkrvmf6wy0o8zjz:59377] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6408ca5ff5]
[pkrvmf6wy0o8zjz:59377] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6408cbb0da]
[pkrvmf6wy0o8zjz:59377] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6408ca5a55]
[pkrvmf6wy0o8zjz:59377] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6408ca5a6f]
[pkrvmf6wy0o8zjz:59377] [ 8] plumed(+0x13209)[0x5644b81b5209]
[pkrvmf6wy0o8zjz:59377] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f640882a1ca]
[pkrvmf6wy0o8zjz:59377] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f640882a28b]
[pkrvmf6wy0o8zjz:59377] [11] plumed(+0x134a5)[0x5644b81b54a5]
[pkrvmf6wy0o8zjz:59377] *** End of error message ***
</pre>
{% endraw %}
