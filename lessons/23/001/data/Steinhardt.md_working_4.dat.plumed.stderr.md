Stderr for source:  Steinhardt.md_working_4.dat   
Download: [zipped raw stdout](Steinhardt.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIESA=1 SPECIESB=2-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:59688] *** Process received signal ***
[pkrvmf6wy0o8zjz:59688] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59688] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59688] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff209845330]
[pkrvmf6wy0o8zjz:59688] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff20989eb2c]
[pkrvmf6wy0o8zjz:59688] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff20984527e]
[pkrvmf6wy0o8zjz:59688] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff2098288ff]
[pkrvmf6wy0o8zjz:59688] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff209ca5ff5]
[pkrvmf6wy0o8zjz:59688] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff209cbb0da]
[pkrvmf6wy0o8zjz:59688] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff209ca5a55]
[pkrvmf6wy0o8zjz:59688] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff209ca5a6f]
[pkrvmf6wy0o8zjz:59688] [ 8] plumed(+0x13209)[0x5627584bc209]
[pkrvmf6wy0o8zjz:59688] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff20982a1ca]
[pkrvmf6wy0o8zjz:59688] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff20982a28b]
[pkrvmf6wy0o8zjz:59688] [11] plumed(+0x134a5)[0x5627584bc4a5]
[pkrvmf6wy0o8zjz:59688] *** End of error message ***
</pre>
{% endraw %}
