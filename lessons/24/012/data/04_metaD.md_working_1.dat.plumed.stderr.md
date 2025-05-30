Stderr for source:  04_metaD.md_working_1.dat   
Download: [zipped raw stdout](04_metaD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](04_metaD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: [TORSION](HTTPS://WWW.PLUMED.ORG/DOC-MASTER/USER-DOC/HTML/_T_O_R_S_I_O_N.HTML) LABEL=t1 ATOMS=1,6,4,5
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:59057] *** Process received signal ***
[pkrvmf6wy0o8zjz:59057] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59057] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59057] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff9ace45330]
[pkrvmf6wy0o8zjz:59057] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff9ace9eb2c]
[pkrvmf6wy0o8zjz:59057] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff9ace4527e]
[pkrvmf6wy0o8zjz:59057] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff9ace288ff]
[pkrvmf6wy0o8zjz:59057] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff9ad2a5ff5]
[pkrvmf6wy0o8zjz:59057] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff9ad2bb0da]
[pkrvmf6wy0o8zjz:59057] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff9ad2a5a55]
[pkrvmf6wy0o8zjz:59057] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff9ad2a5a6f]
[pkrvmf6wy0o8zjz:59057] [ 8] plumed(+0x13209)[0x5615852ac209]
[pkrvmf6wy0o8zjz:59057] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff9ace2a1ca]
[pkrvmf6wy0o8zjz:59057] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff9ace2a28b]
[pkrvmf6wy0o8zjz:59057] [11] plumed(+0x134a5)[0x5615852ac4a5]
[pkrvmf6wy0o8zjz:59057] *** End of error message ***
</pre>
{% endraw %}
