Stderr for source:  input.md_working_3.dat   
Download: [zipped raw stdout](input.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](input.md_working_3.dat.plumed.stderr.txt.zip) 
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
[pkrvmbietmlfzoi:35194] *** Process received signal ***
[pkrvmbietmlfzoi:35194] Signal: Aborted (6)
[pkrvmbietmlfzoi:35194] Signal code:  (-6)
[pkrvmbietmlfzoi:35194] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb145245330]
[pkrvmbietmlfzoi:35194] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb14529eb2c]
[pkrvmbietmlfzoi:35194] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb14524527e]
[pkrvmbietmlfzoi:35194] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb1452288ff]
[pkrvmbietmlfzoi:35194] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb1456a5ff5]
[pkrvmbietmlfzoi:35194] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb1456bb0da]
[pkrvmbietmlfzoi:35194] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb1456a5a55]
[pkrvmbietmlfzoi:35194] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb1456a5a6f]
[pkrvmbietmlfzoi:35194] [ 8] plumed(+0x13209)[0x55869b938209]
[pkrvmbietmlfzoi:35194] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb14522a1ca]
[pkrvmbietmlfzoi:35194] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb14522a28b]
[pkrvmbietmlfzoi:35194] [11] plumed(+0x134a5)[0x55869b9384a5]
[pkrvmbietmlfzoi:35194] *** End of error message ***
</pre>
{% endraw %}
