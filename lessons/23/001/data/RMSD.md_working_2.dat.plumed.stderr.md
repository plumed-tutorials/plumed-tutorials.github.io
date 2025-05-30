Stderr for source:  RMSD.md_working_2.dat   
Download: [zipped raw stdout](RMSD.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DISPLACEMENT LABEL=disp ARG1=d1,d2,d3 ARG2=d1_ref,d2_ref,d3_ref
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61648] *** Process received signal ***
[pkrvmf6wy0o8zjz:61648] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61648] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61648] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff2d6c45330]
[pkrvmf6wy0o8zjz:61648] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff2d6c9eb2c]
[pkrvmf6wy0o8zjz:61648] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff2d6c4527e]
[pkrvmf6wy0o8zjz:61648] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff2d6c288ff]
[pkrvmf6wy0o8zjz:61648] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff2d70a5ff5]
[pkrvmf6wy0o8zjz:61648] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff2d70bb0da]
[pkrvmf6wy0o8zjz:61648] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff2d70a5a55]
[pkrvmf6wy0o8zjz:61648] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff2d70a5a6f]
[pkrvmf6wy0o8zjz:61648] [ 8] plumed(+0x13209)[0x563cdb2fb209]
[pkrvmf6wy0o8zjz:61648] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff2d6c2a1ca]
[pkrvmf6wy0o8zjz:61648] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff2d6c2a28b]
[pkrvmf6wy0o8zjz:61648] [11] plumed(+0x134a5)[0x563cdb2fb4a5]
[pkrvmf6wy0o8zjz:61648] *** End of error message ***
</pre>
{% endraw %}
