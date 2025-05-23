Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:58803] *** Process received signal ***
[pkrvmf6wy0o8zjz:58803] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58803] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58803] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1fa8645330]
[pkrvmf6wy0o8zjz:58803] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1fa869eb2c]
[pkrvmf6wy0o8zjz:58803] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1fa864527e]
[pkrvmf6wy0o8zjz:58803] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1fa86288ff]
[pkrvmf6wy0o8zjz:58803] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1fa8aa5ff5]
[pkrvmf6wy0o8zjz:58803] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1fa8abb0da]
[pkrvmf6wy0o8zjz:58803] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1fa8aa5a55]
[pkrvmf6wy0o8zjz:58803] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1fa8aa5a6f]
[pkrvmf6wy0o8zjz:58803] [ 8] plumed(+0x13209)[0x56175ab48209]
[pkrvmf6wy0o8zjz:58803] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1fa862a1ca]
[pkrvmf6wy0o8zjz:58803] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1fa862a28b]
[pkrvmf6wy0o8zjz:58803] [11] plumed(+0x134a5)[0x56175ab484a5]
[pkrvmf6wy0o8zjz:58803] *** End of error message ***
</pre>
{% endraw %}
