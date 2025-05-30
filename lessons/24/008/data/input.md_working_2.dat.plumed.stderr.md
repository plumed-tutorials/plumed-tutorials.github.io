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
[pkrvmf6wy0o8zjz:59150] *** Process received signal ***
[pkrvmf6wy0o8zjz:59150] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59150] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59150] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb6fe045330]
[pkrvmf6wy0o8zjz:59150] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb6fe09eb2c]
[pkrvmf6wy0o8zjz:59150] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb6fe04527e]
[pkrvmf6wy0o8zjz:59150] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb6fe0288ff]
[pkrvmf6wy0o8zjz:59150] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb6fe4a5ff5]
[pkrvmf6wy0o8zjz:59150] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb6fe4bb0da]
[pkrvmf6wy0o8zjz:59150] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb6fe4a5a55]
[pkrvmf6wy0o8zjz:59150] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb6fe4a5a6f]
[pkrvmf6wy0o8zjz:59150] [ 8] plumed(+0x13209)[0x55d2a7d5e209]
[pkrvmf6wy0o8zjz:59150] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb6fe02a1ca]
[pkrvmf6wy0o8zjz:59150] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb6fe02a28b]
[pkrvmf6wy0o8zjz:59150] [11] plumed(+0x134a5)[0x55d2a7d5e4a5]
[pkrvmf6wy0o8zjz:59150] *** End of error message ***
</pre>
{% endraw %}
