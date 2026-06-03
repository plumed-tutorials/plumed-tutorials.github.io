Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervm3jyl0:48794] *** Process received signal ***
[runnervm3jyl0:48794] Signal: Aborted (6)
[runnervm3jyl0:48794] Signal code:  (-6)
[runnervm3jyl0:48794] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f56f8445330]
[runnervm3jyl0:48794] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f56f849eb2c]
[runnervm3jyl0:48794] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f56f844527e]
[runnervm3jyl0:48794] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f56f84288ff]
[runnervm3jyl0:48794] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f56f88a5ff5]
[runnervm3jyl0:48794] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f56f88bb0da]
[runnervm3jyl0:48794] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f56f88a5a55]
[runnervm3jyl0:48794] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f56f88a5a6f]
[runnervm3jyl0:48794] [ 8] plumed_master(+0x146dd)[0x5576353156dd]
[runnervm3jyl0:48794] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f56f842a1ca]
[runnervm3jyl0:48794] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f56f842a28b]
[runnervm3jyl0:48794] [11] plumed_master(+0x15365)[0x557635316365]
[runnervm3jyl0:48794] *** End of error message ***
</pre>
{% endraw %}
