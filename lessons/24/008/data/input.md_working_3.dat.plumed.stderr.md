Stderr for source:  input.md_working_3.dat   
Download: [zipped raw stdout](input.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](input.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MAZE_OPT_ANNEALING LABEL=opt GROUPA=group_bnz GROUPB=group_t4l SWITCH=EXP R_0=0.2 STRIDE=500000 N_ITER=1000 BETA=0.9 BETA_FACTOR=1.005 BETA_SCHEDULE=GEOM RANDOM_SEED=111 NLIST NL_CUTOFF=0.6 NL_STRIDE=100
Maybe a missing space or a typo?
[fv-az1778-96:04511] *** Process received signal ***
[fv-az1778-96:04511] Signal: Aborted (6)
[fv-az1778-96:04511] Signal code:  (-6)
[fv-az1778-96:04511] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd2fb842520]
[fv-az1778-96:04511] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd2fb8969fc]
[fv-az1778-96:04511] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd2fb842476]
[fv-az1778-96:04511] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd2fb8287f3]
[fv-az1778-96:04511] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd2fbca2b9e]
[fv-az1778-96:04511] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd2fbcae20c]
[fv-az1778-96:04511] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd2fbcae277]
[fv-az1778-96:04511] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd2fbcae52b]
[fv-az1778-96:04511] [ 8] plumed(+0x12f48)[0x562100b32f48]
[fv-az1778-96:04511] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd2fb829d90]
[fv-az1778-96:04511] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd2fb829e40]
[fv-az1778-96:04511] [11] plumed(+0x131e5)[0x562100b331e5]
[fv-az1778-96:04511] *** End of error message ***
</pre>
{% endraw %}
