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
[pkrvmf6wy0o8zjz:59176] *** Process received signal ***
[pkrvmf6wy0o8zjz:59176] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59176] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59176] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f93e6645330]
[pkrvmf6wy0o8zjz:59176] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f93e669eb2c]
[pkrvmf6wy0o8zjz:59176] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f93e664527e]
[pkrvmf6wy0o8zjz:59176] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f93e66288ff]
[pkrvmf6wy0o8zjz:59176] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f93e6aa5ff5]
[pkrvmf6wy0o8zjz:59176] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f93e6abb0da]
[pkrvmf6wy0o8zjz:59176] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f93e6aa5a55]
[pkrvmf6wy0o8zjz:59176] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f93e6aa5a6f]
[pkrvmf6wy0o8zjz:59176] [ 8] plumed(+0x13209)[0x561ebe380209]
[pkrvmf6wy0o8zjz:59176] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f93e662a1ca]
[pkrvmf6wy0o8zjz:59176] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f93e662a28b]
[pkrvmf6wy0o8zjz:59176] [11] plumed(+0x134a5)[0x561ebe3804a5]
[pkrvmf6wy0o8zjz:59176] *** End of error message ***
</pre>
{% endraw %}
