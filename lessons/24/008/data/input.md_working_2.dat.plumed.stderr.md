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
[fv-az1755-505:05508] *** Process received signal ***
[fv-az1755-505:05508] Signal: Aborted (6)
[fv-az1755-505:05508] Signal code:  (-6)
[fv-az1755-505:05508] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbe2ce45330]
[fv-az1755-505:05508] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbe2ce9eb2c]
[fv-az1755-505:05508] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbe2ce4527e]
[fv-az1755-505:05508] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbe2ce288ff]
[fv-az1755-505:05508] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbe2d2a5ff5]
[fv-az1755-505:05508] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbe2d2bb0da]
[fv-az1755-505:05508] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbe2d2a5a55]
[fv-az1755-505:05508] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbe2d2a5a6f]
[fv-az1755-505:05508] [ 8] plumed(+0x13209)[0x55c659499209]
[fv-az1755-505:05508] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbe2ce2a1ca]
[fv-az1755-505:05508] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbe2ce2a28b]
[fv-az1755-505:05508] [11] plumed(+0x134a5)[0x55c6594994a5]
[fv-az1755-505:05508] *** End of error message ***
</pre>
{% endraw %}
