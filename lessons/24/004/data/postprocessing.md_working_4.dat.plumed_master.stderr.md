Stderr for source:  postprocessing.md_working_4.dat   
Download: [zipped raw stdout](postprocessing.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action HISTOGRAM with label @s14 : set NORMALIZATION=true/false when using LOGWEIGHTS as otherwise the weights are ignored. Alternatively, learn to use the new syntax for histograms with KDE/ACCUMULATE to have more control over what PLUMED is calculating
[runnervm3jyl0:47650] *** Process received signal ***
[runnervm3jyl0:47650] Signal: Aborted (6)
[runnervm3jyl0:47650] Signal code:  (-6)
[runnervm3jyl0:47650] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb5f3c45330]
[runnervm3jyl0:47650] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb5f3c9eb2c]
[runnervm3jyl0:47650] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb5f3c4527e]
[runnervm3jyl0:47650] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb5f3c288ff]
[runnervm3jyl0:47650] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb5f40a5ff5]
[runnervm3jyl0:47650] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb5f40bb0da]
[runnervm3jyl0:47650] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb5f40a5a55]
[runnervm3jyl0:47650] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb5f40a5a6f]
[runnervm3jyl0:47650] [ 8] plumed_master(+0x146dd)[0x5588d7acb6dd]
[runnervm3jyl0:47650] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb5f3c2a1ca]
[runnervm3jyl0:47650] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb5f3c2a28b]
[runnervm3jyl0:47650] [11] plumed_master(+0x15365)[0x5588d7acc365]
[runnervm3jyl0:47650] *** End of error message ***
</pre>
{% endraw %}
