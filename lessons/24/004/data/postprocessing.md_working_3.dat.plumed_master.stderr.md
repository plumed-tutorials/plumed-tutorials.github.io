Stderr for source:  postprocessing.md_working_3.dat   
Download: [zipped raw stdout](postprocessing.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_3.dat.plumed_master.stderr.txt.zip) 
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
[runnervm3jyl0:47619] *** Process received signal ***
[runnervm3jyl0:47619] Signal: Aborted (6)
[runnervm3jyl0:47619] Signal code:  (-6)
[runnervm3jyl0:47619] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9985245330]
[runnervm3jyl0:47619] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f998529eb2c]
[runnervm3jyl0:47619] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f998524527e]
[runnervm3jyl0:47619] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f99852288ff]
[runnervm3jyl0:47619] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f99856a5ff5]
[runnervm3jyl0:47619] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f99856bb0da]
[runnervm3jyl0:47619] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f99856a5a55]
[runnervm3jyl0:47619] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f99856a5a6f]
[runnervm3jyl0:47619] [ 8] plumed_master(+0x146dd)[0x5563c52506dd]
[runnervm3jyl0:47619] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f998522a1ca]
[runnervm3jyl0:47619] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f998522a28b]
[runnervm3jyl0:47619] [11] plumed_master(+0x15365)[0x5563c5251365]
[runnervm3jyl0:47619] *** End of error message ***
</pre>
{% endraw %}
