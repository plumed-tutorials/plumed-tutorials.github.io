Stderr for source:  GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cvPY ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:58762] *** Process received signal ***
[pkrvmf6wy0o8zjz:58762] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58762] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58762] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb75f645330]
[pkrvmf6wy0o8zjz:58762] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb75f69eb2c]
[pkrvmf6wy0o8zjz:58762] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb75f64527e]
[pkrvmf6wy0o8zjz:58762] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb75f6288ff]
[pkrvmf6wy0o8zjz:58762] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb75faa5ff5]
[pkrvmf6wy0o8zjz:58762] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb75fabb0da]
[pkrvmf6wy0o8zjz:58762] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb75faa5a55]
[pkrvmf6wy0o8zjz:58762] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb75faa5a6f]
[pkrvmf6wy0o8zjz:58762] [ 8] plumed(+0x13209)[0x55f7b8466209]
[pkrvmf6wy0o8zjz:58762] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb75f62a1ca]
[pkrvmf6wy0o8zjz:58762] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb75f62a28b]
[pkrvmf6wy0o8zjz:58762] [11] plumed(+0x134a5)[0x55f7b84664a5]
[pkrvmf6wy0o8zjz:58762] *** End of error message ***
</pre>
{% endraw %}
