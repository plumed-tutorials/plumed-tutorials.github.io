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
[runnervmg397c:79474] *** Process received signal ***
[runnervmg397c:79474] Signal: Aborted (6)
[runnervmg397c:79474] Signal code:  (-6)
[runnervmg397c:79474] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1a54045330]
[runnervmg397c:79474] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1a5409eb2c]
[runnervmg397c:79474] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1a5404527e]
[runnervmg397c:79474] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1a540288ff]
[runnervmg397c:79474] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1a544a5ff5]
[runnervmg397c:79474] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1a544bb0da]
[runnervmg397c:79474] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1a544a5a55]
[runnervmg397c:79474] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1a544a5a6f]
[runnervmg397c:79474] [ 8] plumed(+0x13209)[0x564aafe09209]
[runnervmg397c:79474] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1a5402a1ca]
[runnervmg397c:79474] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1a5402a28b]
[runnervmg397c:79474] [11] plumed(+0x134a5)[0x564aafe094a5]
[runnervmg397c:79474] *** End of error message ***
</pre>
{% endraw %}
