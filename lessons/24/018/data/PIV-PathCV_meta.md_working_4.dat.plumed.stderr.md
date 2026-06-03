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
[runnervm3jyl0:47312] *** Process received signal ***
[runnervm3jyl0:47312] Signal: Aborted (6)
[runnervm3jyl0:47312] Signal code:  (-6)
[runnervm3jyl0:47312] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efde3a45330]
[runnervm3jyl0:47312] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efde3a9eb2c]
[runnervm3jyl0:47312] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efde3a4527e]
[runnervm3jyl0:47312] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efde3a288ff]
[runnervm3jyl0:47312] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efde3ea5ff5]
[runnervm3jyl0:47312] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efde3ebb0da]
[runnervm3jyl0:47312] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efde3ea5a55]
[runnervm3jyl0:47312] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efde3ea5a6f]
[runnervm3jyl0:47312] [ 8] plumed(+0x13209)[0x556112c69209]
[runnervm3jyl0:47312] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efde3a2a1ca]
[runnervm3jyl0:47312] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efde3a2a28b]
[runnervm3jyl0:47312] [11] plumed(+0x134a5)[0x556112c694a5]
[runnervm3jyl0:47312] *** End of error message ***
</pre>
{% endraw %}
