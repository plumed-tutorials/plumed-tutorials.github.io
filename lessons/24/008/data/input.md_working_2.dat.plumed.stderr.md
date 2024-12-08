Stderr for source:  input.md_working_2.dat   
Download: [zipped raw stdout](input.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](input.md_working_2.dat.plumed.stderr.txt.zip) 
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
[fv-az1778-96:04488] *** Process received signal ***
[fv-az1778-96:04488] Signal: Aborted (6)
[fv-az1778-96:04488] Signal code:  (-6)
[fv-az1778-96:04488] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4e40e42520]
[fv-az1778-96:04488] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4e40e969fc]
[fv-az1778-96:04488] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4e40e42476]
[fv-az1778-96:04488] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4e40e287f3]
[fv-az1778-96:04488] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4e412a2b9e]
[fv-az1778-96:04488] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4e412ae20c]
[fv-az1778-96:04488] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4e412ae277]
[fv-az1778-96:04488] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4e412ae52b]
[fv-az1778-96:04488] [ 8] plumed(+0x12f48)[0x55893d1fbf48]
[fv-az1778-96:04488] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4e40e29d90]
[fv-az1778-96:04488] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4e40e29e40]
[fv-az1778-96:04488] [11] plumed(+0x131e5)[0x55893d1fc1e5]
[fv-az1778-96:04488] *** End of error message ***
</pre>
{% endraw %}
