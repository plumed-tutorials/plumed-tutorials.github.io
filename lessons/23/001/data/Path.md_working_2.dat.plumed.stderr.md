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
[pkrvmf6wy0o8zjz:61599] *** Process received signal ***
[pkrvmf6wy0o8zjz:61599] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61599] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61599] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa462e45330]
[pkrvmf6wy0o8zjz:61599] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa462e9eb2c]
[pkrvmf6wy0o8zjz:61599] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa462e4527e]
[pkrvmf6wy0o8zjz:61599] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa462e288ff]
[pkrvmf6wy0o8zjz:61599] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa4632a5ff5]
[pkrvmf6wy0o8zjz:61599] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa4632bb0da]
[pkrvmf6wy0o8zjz:61599] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa4632a5a55]
[pkrvmf6wy0o8zjz:61599] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa4632a5a6f]
[pkrvmf6wy0o8zjz:61599] [ 8] plumed(+0x13209)[0x55bc2ee13209]
[pkrvmf6wy0o8zjz:61599] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa462e2a1ca]
[pkrvmf6wy0o8zjz:61599] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa462e2a28b]
[pkrvmf6wy0o8zjz:61599] [11] plumed(+0x134a5)[0x55bc2ee134a5]
[pkrvmf6wy0o8zjz:61599] *** End of error message ***
</pre>
{% endraw %}
