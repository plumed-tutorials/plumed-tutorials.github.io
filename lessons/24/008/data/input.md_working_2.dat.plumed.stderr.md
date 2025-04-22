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
[fv-az1279-640:05750] *** Process received signal ***
[fv-az1279-640:05750] Signal: Aborted (6)
[fv-az1279-640:05750] Signal code:  (-6)
[fv-az1279-640:05750] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2ae6845330]
[fv-az1279-640:05750] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2ae689eb2c]
[fv-az1279-640:05750] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2ae684527e]
[fv-az1279-640:05750] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2ae68288ff]
[fv-az1279-640:05750] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2ae6ca5ff5]
[fv-az1279-640:05750] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2ae6cbb0da]
[fv-az1279-640:05750] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2ae6ca5a55]
[fv-az1279-640:05750] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2ae6ca5a6f]
[fv-az1279-640:05750] [ 8] plumed(+0x13209)[0x55d03c682209]
[fv-az1279-640:05750] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2ae682a1ca]
[fv-az1279-640:05750] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2ae682a28b]
[fv-az1279-640:05750] [11] plumed(+0x134a5)[0x55d03c6824a5]
[fv-az1279-640:05750] *** End of error message ***
</pre>
{% endraw %}
