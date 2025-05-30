Stderr for source:  Steinhardt.md_working_19.dat   
Download: [zipped raw stdout](Steinhardt.md_working_19.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_19.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60220] *** Process received signal ***
[pkrvmf6wy0o8zjz:60220] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60220] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60220] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f56d2645330]
[pkrvmf6wy0o8zjz:60220] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f56d269eb2c]
[pkrvmf6wy0o8zjz:60220] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f56d264527e]
[pkrvmf6wy0o8zjz:60220] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f56d26288ff]
[pkrvmf6wy0o8zjz:60220] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f56d2aa5ff5]
[pkrvmf6wy0o8zjz:60220] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f56d2abb0da]
[pkrvmf6wy0o8zjz:60220] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f56d2aa5a55]
[pkrvmf6wy0o8zjz:60220] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f56d2aa5a6f]
[pkrvmf6wy0o8zjz:60220] [ 8] plumed(+0x13209)[0x55daee658209]
[pkrvmf6wy0o8zjz:60220] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f56d262a1ca]
[pkrvmf6wy0o8zjz:60220] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f56d262a28b]
[pkrvmf6wy0o8zjz:60220] [11] plumed(+0x134a5)[0x55daee6584a5]
[pkrvmf6wy0o8zjz:60220] *** End of error message ***
</pre>
{% endraw %}
