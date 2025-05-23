Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.4 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60049] *** Process received signal ***
[pkrvmf6wy0o8zjz:60049] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60049] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60049] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f41a9045330]
[pkrvmf6wy0o8zjz:60049] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f41a909eb2c]
[pkrvmf6wy0o8zjz:60049] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f41a904527e]
[pkrvmf6wy0o8zjz:60049] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f41a90288ff]
[pkrvmf6wy0o8zjz:60049] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f41a94a5ff5]
[pkrvmf6wy0o8zjz:60049] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f41a94bb0da]
[pkrvmf6wy0o8zjz:60049] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f41a94a5a55]
[pkrvmf6wy0o8zjz:60049] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f41a94a5a6f]
[pkrvmf6wy0o8zjz:60049] [ 8] plumed(+0x13209)[0x55d7046ba209]
[pkrvmf6wy0o8zjz:60049] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f41a902a1ca]
[pkrvmf6wy0o8zjz:60049] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f41a902a28b]
[pkrvmf6wy0o8zjz:60049] [11] plumed(+0x134a5)[0x55d7046ba4a5]
[pkrvmf6wy0o8zjz:60049] *** End of error message ***
</pre>
{% endraw %}
