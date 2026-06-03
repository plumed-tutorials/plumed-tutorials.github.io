Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed.stderr.txt.zip) 
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
[runnervm3jyl0:47854] *** Process received signal ***
[runnervm3jyl0:47854] Signal: Aborted (6)
[runnervm3jyl0:47854] Signal code:  (-6)
[runnervm3jyl0:47854] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1260245330]
[runnervm3jyl0:47854] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f126029eb2c]
[runnervm3jyl0:47854] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f126024527e]
[runnervm3jyl0:47854] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f12602288ff]
[runnervm3jyl0:47854] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f12606a5ff5]
[runnervm3jyl0:47854] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f12606bb0da]
[runnervm3jyl0:47854] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f12606a5a55]
[runnervm3jyl0:47854] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f12606a5a6f]
[runnervm3jyl0:47854] [ 8] plumed(+0x13209)[0x561ca0db9209]
[runnervm3jyl0:47854] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f126022a1ca]
[runnervm3jyl0:47854] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f126022a28b]
[runnervm3jyl0:47854] [11] plumed(+0x134a5)[0x561ca0db94a5]
[runnervm3jyl0:47854] *** End of error message ***
</pre>
{% endraw %}
