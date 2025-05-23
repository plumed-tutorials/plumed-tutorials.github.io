Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.5 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60005] *** Process received signal ***
[pkrvmf6wy0o8zjz:60005] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60005] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60005] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa874a45330]
[pkrvmf6wy0o8zjz:60005] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa874a9eb2c]
[pkrvmf6wy0o8zjz:60005] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa874a4527e]
[pkrvmf6wy0o8zjz:60005] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa874a288ff]
[pkrvmf6wy0o8zjz:60005] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa874ea5ff5]
[pkrvmf6wy0o8zjz:60005] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa874ebb0da]
[pkrvmf6wy0o8zjz:60005] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa874ea5a55]
[pkrvmf6wy0o8zjz:60005] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa874ea5a6f]
[pkrvmf6wy0o8zjz:60005] [ 8] plumed(+0x13209)[0x5593e2958209]
[pkrvmf6wy0o8zjz:60005] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa874a2a1ca]
[pkrvmf6wy0o8zjz:60005] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa874a2a28b]
[pkrvmf6wy0o8zjz:60005] [11] plumed(+0x134a5)[0x5593e29584a5]
[pkrvmf6wy0o8zjz:60005] *** End of error message ***
</pre>
{% endraw %}
