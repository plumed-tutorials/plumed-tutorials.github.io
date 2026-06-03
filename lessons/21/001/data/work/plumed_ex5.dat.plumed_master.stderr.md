Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervm3jyl0:48870] *** Process received signal ***
[runnervm3jyl0:48870] Signal: Aborted (6)
[runnervm3jyl0:48870] Signal code:  (-6)
[runnervm3jyl0:48870] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7237e45330]
[runnervm3jyl0:48870] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7237e9eb2c]
[runnervm3jyl0:48870] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7237e4527e]
[runnervm3jyl0:48870] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7237e288ff]
[runnervm3jyl0:48870] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f72382a5ff5]
[runnervm3jyl0:48870] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f72382bb0da]
[runnervm3jyl0:48870] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f72382a5a55]
[runnervm3jyl0:48870] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f72382a5a6f]
[runnervm3jyl0:48870] [ 8] plumed_master(+0x146dd)[0x55c0946e06dd]
[runnervm3jyl0:48870] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7237e2a1ca]
[runnervm3jyl0:48870] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7237e2a28b]
[runnervm3jyl0:48870] [11] plumed_master(+0x15365)[0x55c0946e1365]
[runnervm3jyl0:48870] *** End of error message ***
</pre>
{% endraw %}
