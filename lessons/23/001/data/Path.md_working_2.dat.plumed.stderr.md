Stderr for source:  Path.md_working_2.dat   
Download: [zipped raw stdout](Path.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: LOWEST LABEL=p_mindist ARG=p_data
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61847] *** Process received signal ***
[pkrvmf6wy0o8zjz:61847] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61847] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61847] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc3e8445330]
[pkrvmf6wy0o8zjz:61847] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc3e849eb2c]
[pkrvmf6wy0o8zjz:61847] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc3e844527e]
[pkrvmf6wy0o8zjz:61847] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc3e84288ff]
[pkrvmf6wy0o8zjz:61847] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc3e88a5ff5]
[pkrvmf6wy0o8zjz:61847] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc3e88bb0da]
[pkrvmf6wy0o8zjz:61847] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc3e88a5a55]
[pkrvmf6wy0o8zjz:61847] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc3e88a5a6f]
[pkrvmf6wy0o8zjz:61847] [ 8] plumed(+0x13209)[0x555ae13d4209]
[pkrvmf6wy0o8zjz:61847] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc3e842a1ca]
[pkrvmf6wy0o8zjz:61847] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc3e842a28b]
[pkrvmf6wy0o8zjz:61847] [11] plumed(+0x134a5)[0x555ae13d44a5]
[pkrvmf6wy0o8zjz:61847] *** End of error message ***
</pre>
{% endraw %}
