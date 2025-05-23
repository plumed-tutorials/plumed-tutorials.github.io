Stderr for source:  PIV-PathCV_meta.md_working_4.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GMX grompp -f md.mdp -c Liq.pdb -p TIP4P.top -o meta.tpr
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:58936] *** Process received signal ***
[pkrvmf6wy0o8zjz:58936] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58936] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58936] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7957a45330]
[pkrvmf6wy0o8zjz:58936] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7957a9eb2c]
[pkrvmf6wy0o8zjz:58936] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7957a4527e]
[pkrvmf6wy0o8zjz:58936] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7957a288ff]
[pkrvmf6wy0o8zjz:58936] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7957ea5ff5]
[pkrvmf6wy0o8zjz:58936] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7957ebb0da]
[pkrvmf6wy0o8zjz:58936] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7957ea5a55]
[pkrvmf6wy0o8zjz:58936] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7957ea5a6f]
[pkrvmf6wy0o8zjz:58936] [ 8] plumed(+0x13209)[0x563ce5cdf209]
[pkrvmf6wy0o8zjz:58936] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7957a2a1ca]
[pkrvmf6wy0o8zjz:58936] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7957a2a28b]
[pkrvmf6wy0o8zjz:58936] [11] plumed(+0x134a5)[0x563ce5cdf4a5]
[pkrvmf6wy0o8zjz:58936] *** End of error message ***
</pre>
{% endraw %}
