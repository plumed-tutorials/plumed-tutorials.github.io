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
[pkrvmf6wy0o8zjz:58804] *** Process received signal ***
[pkrvmf6wy0o8zjz:58804] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58804] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58804] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f373e845330]
[pkrvmf6wy0o8zjz:58804] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f373e89eb2c]
[pkrvmf6wy0o8zjz:58804] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f373e84527e]
[pkrvmf6wy0o8zjz:58804] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f373e8288ff]
[pkrvmf6wy0o8zjz:58804] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f373eca5ff5]
[pkrvmf6wy0o8zjz:58804] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f373ecbb0da]
[pkrvmf6wy0o8zjz:58804] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f373eca5a55]
[pkrvmf6wy0o8zjz:58804] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f373eca5a6f]
[pkrvmf6wy0o8zjz:58804] [ 8] plumed(+0x13209)[0x5570898e2209]
[pkrvmf6wy0o8zjz:58804] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f373e82a1ca]
[pkrvmf6wy0o8zjz:58804] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f373e82a28b]
[pkrvmf6wy0o8zjz:58804] [11] plumed(+0x134a5)[0x5570898e24a5]
[pkrvmf6wy0o8zjz:58804] *** End of error message ***
</pre>
{% endraw %}
