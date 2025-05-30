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
[pkrvmf6wy0o8zjz:60905] *** Process received signal ***
[pkrvmf6wy0o8zjz:60905] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60905] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60905] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f77fa045330]
[pkrvmf6wy0o8zjz:60905] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f77fa09eb2c]
[pkrvmf6wy0o8zjz:60905] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f77fa04527e]
[pkrvmf6wy0o8zjz:60905] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f77fa0288ff]
[pkrvmf6wy0o8zjz:60905] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f77fa4a5ff5]
[pkrvmf6wy0o8zjz:60905] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f77fa4bb0da]
[pkrvmf6wy0o8zjz:60905] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f77fa4a5a55]
[pkrvmf6wy0o8zjz:60905] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f77fa4a5a6f]
[pkrvmf6wy0o8zjz:60905] [ 8] plumed(+0x13209)[0x55afb5eb4209]
[pkrvmf6wy0o8zjz:60905] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f77fa02a1ca]
[pkrvmf6wy0o8zjz:60905] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f77fa02a28b]
[pkrvmf6wy0o8zjz:60905] [11] plumed(+0x134a5)[0x55afb5eb44a5]
[pkrvmf6wy0o8zjz:60905] *** End of error message ***
</pre>
{% endraw %}
