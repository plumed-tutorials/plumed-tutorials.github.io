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
[runnervmg397c:79567] *** Process received signal ***
[runnervmg397c:79567] Signal: Aborted (6)
[runnervmg397c:79567] Signal code:  (-6)
[runnervmg397c:79567] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff732245330]
[runnervmg397c:79567] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff73229eb2c]
[runnervmg397c:79567] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff73224527e]
[runnervmg397c:79567] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff7322288ff]
[runnervmg397c:79567] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff7326a5ff5]
[runnervmg397c:79567] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff7326bb0da]
[runnervmg397c:79567] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff7326a5a55]
[runnervmg397c:79567] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff7326a5a6f]
[runnervmg397c:79567] [ 8] plumed(+0x13209)[0x5585e951a209]
[runnervmg397c:79567] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff73222a1ca]
[runnervmg397c:79567] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff73222a28b]
[runnervmg397c:79567] [11] plumed(+0x134a5)[0x5585e951a4a5]
[runnervmg397c:79567] *** End of error message ***
</pre>
{% endraw %}
