Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61630] *** Process received signal ***
[pkrvmf6wy0o8zjz:61630] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61630] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61630] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f04c8645330]
[pkrvmf6wy0o8zjz:61630] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f04c869eb2c]
[pkrvmf6wy0o8zjz:61630] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f04c864527e]
[pkrvmf6wy0o8zjz:61630] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f04c86288ff]
[pkrvmf6wy0o8zjz:61630] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f04c8aa5ff5]
[pkrvmf6wy0o8zjz:61630] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f04c8abb0da]
[pkrvmf6wy0o8zjz:61630] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f04c8aa5a55]
[pkrvmf6wy0o8zjz:61630] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f04c8aa5a6f]
[pkrvmf6wy0o8zjz:61630] [ 8] plumed(+0x13209)[0x55d6f42e2209]
[pkrvmf6wy0o8zjz:61630] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f04c862a1ca]
[pkrvmf6wy0o8zjz:61630] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f04c862a28b]
[pkrvmf6wy0o8zjz:61630] [11] plumed(+0x134a5)[0x55d6f42e24a5]
[pkrvmf6wy0o8zjz:61630] *** End of error message ***
</pre>
{% endraw %}
