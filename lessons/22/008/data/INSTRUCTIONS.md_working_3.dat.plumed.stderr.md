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
[pkrvmf6wy0o8zjz:60246] *** Process received signal ***
[pkrvmf6wy0o8zjz:60246] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60246] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60246] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdcd6645330]
[pkrvmf6wy0o8zjz:60246] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdcd669eb2c]
[pkrvmf6wy0o8zjz:60246] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdcd664527e]
[pkrvmf6wy0o8zjz:60246] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdcd66288ff]
[pkrvmf6wy0o8zjz:60246] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdcd6aa5ff5]
[pkrvmf6wy0o8zjz:60246] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdcd6abb0da]
[pkrvmf6wy0o8zjz:60246] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdcd6aa5a55]
[pkrvmf6wy0o8zjz:60246] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdcd6aa5a6f]
[pkrvmf6wy0o8zjz:60246] [ 8] plumed(+0x13209)[0x55b302854209]
[pkrvmf6wy0o8zjz:60246] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdcd662a1ca]
[pkrvmf6wy0o8zjz:60246] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdcd662a28b]
[pkrvmf6wy0o8zjz:60246] [11] plumed(+0x134a5)[0x55b3028544a5]
[pkrvmf6wy0o8zjz:60246] *** End of error message ***
</pre>
{% endraw %}
