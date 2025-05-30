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
[pkrvmf6wy0o8zjz:59210] *** Process received signal ***
[pkrvmf6wy0o8zjz:59210] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59210] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59210] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc3b9245330]
[pkrvmf6wy0o8zjz:59210] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc3b929eb2c]
[pkrvmf6wy0o8zjz:59210] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc3b924527e]
[pkrvmf6wy0o8zjz:59210] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc3b92288ff]
[pkrvmf6wy0o8zjz:59210] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc3b96a5ff5]
[pkrvmf6wy0o8zjz:59210] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc3b96bb0da]
[pkrvmf6wy0o8zjz:59210] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc3b96a5a55]
[pkrvmf6wy0o8zjz:59210] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc3b96a5a6f]
[pkrvmf6wy0o8zjz:59210] [ 8] plumed(+0x13209)[0x5610f22fb209]
[pkrvmf6wy0o8zjz:59210] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc3b922a1ca]
[pkrvmf6wy0o8zjz:59210] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc3b922a28b]
[pkrvmf6wy0o8zjz:59210] [11] plumed(+0x134a5)[0x5610f22fb4a5]
[pkrvmf6wy0o8zjz:59210] *** End of error message ***
</pre>
{% endraw %}
