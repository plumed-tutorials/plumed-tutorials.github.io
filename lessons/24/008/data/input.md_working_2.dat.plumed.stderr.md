Stderr for source:  input.md_working_2.dat   
Download: [zipped raw stdout](input.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](input.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MAZE_OPT_ANNEALING LABEL=opt GROUPA=group_bnz GROUPB=group_t4l SWITCH=EXP R_0=0.2 STRIDE=500000 N_ITER=1000 BETA=0.9 BETA_FACTOR=1.005 BETA_SCHEDULE=GEOM RANDOM_SEED=111 NLIST NL_CUTOFF=0.6 NL_STRIDE=100
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35147] *** Process received signal ***
[pkrvmbietmlfzoi:35147] Signal: Aborted (6)
[pkrvmbietmlfzoi:35147] Signal code:  (-6)
[pkrvmbietmlfzoi:35147] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efe15045330]
[pkrvmbietmlfzoi:35147] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efe1509eb2c]
[pkrvmbietmlfzoi:35147] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efe1504527e]
[pkrvmbietmlfzoi:35147] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efe150288ff]
[pkrvmbietmlfzoi:35147] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efe154a5ff5]
[pkrvmbietmlfzoi:35147] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efe154bb0da]
[pkrvmbietmlfzoi:35147] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efe154a5a55]
[pkrvmbietmlfzoi:35147] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efe154a5a6f]
[pkrvmbietmlfzoi:35147] [ 8] plumed(+0x13209)[0x55d46d30d209]
[pkrvmbietmlfzoi:35147] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efe1502a1ca]
[pkrvmbietmlfzoi:35147] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efe1502a28b]
[pkrvmbietmlfzoi:35147] [11] plumed(+0x134a5)[0x55d46d30d4a5]
[pkrvmbietmlfzoi:35147] *** End of error message ***
</pre>
{% endraw %}
