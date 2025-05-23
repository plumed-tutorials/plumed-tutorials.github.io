Stderr for source:  averaging.md_working_6.dat   
Download: [zipped raw stdout](averaging.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60654] *** Process received signal ***
[pkrvmf6wy0o8zjz:60654] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60654] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60654] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fea65045330]
[pkrvmf6wy0o8zjz:60654] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fea6509eb2c]
[pkrvmf6wy0o8zjz:60654] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fea6504527e]
[pkrvmf6wy0o8zjz:60654] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fea650288ff]
[pkrvmf6wy0o8zjz:60654] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fea654a5ff5]
[pkrvmf6wy0o8zjz:60654] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fea654bb0da]
[pkrvmf6wy0o8zjz:60654] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fea654a5a55]
[pkrvmf6wy0o8zjz:60654] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fea654a5a6f]
[pkrvmf6wy0o8zjz:60654] [ 8] plumed(+0x13209)[0x56483339a209]
[pkrvmf6wy0o8zjz:60654] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fea6502a1ca]
[pkrvmf6wy0o8zjz:60654] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fea6502a28b]
[pkrvmf6wy0o8zjz:60654] [11] plumed(+0x134a5)[0x56483339a4a5]
[pkrvmf6wy0o8zjz:60654] *** End of error message ***
</pre>
{% endraw %}
