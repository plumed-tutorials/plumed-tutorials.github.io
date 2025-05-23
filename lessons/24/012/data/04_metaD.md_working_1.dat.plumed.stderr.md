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
[pkrvmf6wy0o8zjz:59019] *** Process received signal ***
[pkrvmf6wy0o8zjz:59019] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59019] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59019] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa348645330]
[pkrvmf6wy0o8zjz:59019] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa34869eb2c]
[pkrvmf6wy0o8zjz:59019] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa34864527e]
[pkrvmf6wy0o8zjz:59019] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa3486288ff]
[pkrvmf6wy0o8zjz:59019] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa348aa5ff5]
[pkrvmf6wy0o8zjz:59019] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa348abb0da]
[pkrvmf6wy0o8zjz:59019] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa348aa5a55]
[pkrvmf6wy0o8zjz:59019] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa348aa5a6f]
[pkrvmf6wy0o8zjz:59019] [ 8] plumed(+0x13209)[0x561265b9f209]
[pkrvmf6wy0o8zjz:59019] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa34862a1ca]
[pkrvmf6wy0o8zjz:59019] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa34862a28b]
[pkrvmf6wy0o8zjz:59019] [11] plumed(+0x134a5)[0x561265b9f4a5]
[pkrvmf6wy0o8zjz:59019] *** End of error message ***
</pre>
{% endraw %}
