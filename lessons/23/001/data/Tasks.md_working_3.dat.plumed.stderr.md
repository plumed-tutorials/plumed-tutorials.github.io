Stderr for source:  Tasks.md_working_3.dat   
Download: [zipped raw stdout](Tasks.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones SIZE=100
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:59195] *** Process received signal ***
[pkrvmf6wy0o8zjz:59195] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59195] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59195] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff719645330]
[pkrvmf6wy0o8zjz:59195] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff71969eb2c]
[pkrvmf6wy0o8zjz:59195] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff71964527e]
[pkrvmf6wy0o8zjz:59195] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff7196288ff]
[pkrvmf6wy0o8zjz:59195] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff719aa5ff5]
[pkrvmf6wy0o8zjz:59195] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff719abb0da]
[pkrvmf6wy0o8zjz:59195] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff719aa5a55]
[pkrvmf6wy0o8zjz:59195] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff719aa5a6f]
[pkrvmf6wy0o8zjz:59195] [ 8] plumed(+0x13209)[0x563b083ba209]
[pkrvmf6wy0o8zjz:59195] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff71962a1ca]
[pkrvmf6wy0o8zjz:59195] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff71962a28b]
[pkrvmf6wy0o8zjz:59195] [11] plumed(+0x134a5)[0x563b083ba4a5]
[pkrvmf6wy0o8zjz:59195] *** End of error message ***
</pre>
{% endraw %}
