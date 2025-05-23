Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60784] *** Process received signal ***
[pkrvmf6wy0o8zjz:60784] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60784] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60784] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0d8cc45330]
[pkrvmf6wy0o8zjz:60784] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0d8cc9eb2c]
[pkrvmf6wy0o8zjz:60784] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0d8cc4527e]
[pkrvmf6wy0o8zjz:60784] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0d8cc288ff]
[pkrvmf6wy0o8zjz:60784] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0d8d0a5ff5]
[pkrvmf6wy0o8zjz:60784] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0d8d0bb0da]
[pkrvmf6wy0o8zjz:60784] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0d8d0a5a55]
[pkrvmf6wy0o8zjz:60784] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0d8d0a5a6f]
[pkrvmf6wy0o8zjz:60784] [ 8] plumed(+0x13209)[0x55e091fc3209]
[pkrvmf6wy0o8zjz:60784] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0d8cc2a1ca]
[pkrvmf6wy0o8zjz:60784] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0d8cc2a28b]
[pkrvmf6wy0o8zjz:60784] [11] plumed(+0x134a5)[0x55e091fc34a5]
[pkrvmf6wy0o8zjz:60784] *** End of error message ***
</pre>
{% endraw %}
