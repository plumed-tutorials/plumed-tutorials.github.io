Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DUMPPDB ATOMS=cc_data ATOM_INDICES=@nonhydrogens FILE=traj.pdb
Maybe a missing space or a typo?
[runnervm3jyl0:47761] *** Process received signal ***
[runnervm3jyl0:47761] Signal: Aborted (6)
[runnervm3jyl0:47761] Signal code:  (-6)
[runnervm3jyl0:47761] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe0c8c45330]
[runnervm3jyl0:47761] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe0c8c9eb2c]
[runnervm3jyl0:47761] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe0c8c4527e]
[runnervm3jyl0:47761] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe0c8c288ff]
[runnervm3jyl0:47761] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe0c90a5ff5]
[runnervm3jyl0:47761] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe0c90bb0da]
[runnervm3jyl0:47761] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe0c90a5a55]
[runnervm3jyl0:47761] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe0c90a5a6f]
[runnervm3jyl0:47761] [ 8] plumed(+0x13209)[0x55632d488209]
[runnervm3jyl0:47761] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe0c8c2a1ca]
[runnervm3jyl0:47761] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe0c8c2a28b]
[runnervm3jyl0:47761] [11] plumed(+0x134a5)[0x55632d4884a5]
[runnervm3jyl0:47761] *** End of error message ***
</pre>
{% endraw %}
