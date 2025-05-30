Stderr for source:  Steinhardt.md_working_22.dat   
Download: [zipped raw stdout](Steinhardt.md_working_22.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_22.dat.plumed.stderr.txt.zip) 
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
[pkrvmf6wy0o8zjz:60315] *** Process received signal ***
[pkrvmf6wy0o8zjz:60315] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60315] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60315] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa1b0a45330]
[pkrvmf6wy0o8zjz:60315] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa1b0a9eb2c]
[pkrvmf6wy0o8zjz:60315] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa1b0a4527e]
[pkrvmf6wy0o8zjz:60315] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa1b0a288ff]
[pkrvmf6wy0o8zjz:60315] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa1b0ea5ff5]
[pkrvmf6wy0o8zjz:60315] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa1b0ebb0da]
[pkrvmf6wy0o8zjz:60315] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa1b0ea5a55]
[pkrvmf6wy0o8zjz:60315] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa1b0ea5a6f]
[pkrvmf6wy0o8zjz:60315] [ 8] plumed(+0x13209)[0x5575b13ad209]
[pkrvmf6wy0o8zjz:60315] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa1b0a2a1ca]
[pkrvmf6wy0o8zjz:60315] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa1b0a2a28b]
[pkrvmf6wy0o8zjz:60315] [11] plumed(+0x134a5)[0x5575b13ad4a5]
[pkrvmf6wy0o8zjz:60315] *** End of error message ***
</pre>
{% endraw %}
