Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervm3jyl0:48848] *** Process received signal ***
[runnervm3jyl0:48848] Signal: Aborted (6)
[runnervm3jyl0:48848] Signal code:  (-6)
[runnervm3jyl0:48848] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffab8445330]
[runnervm3jyl0:48848] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffab849eb2c]
[runnervm3jyl0:48848] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffab844527e]
[runnervm3jyl0:48848] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffab84288ff]
[runnervm3jyl0:48848] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffab88a5ff5]
[runnervm3jyl0:48848] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffab88bb0da]
[runnervm3jyl0:48848] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffab88a5a55]
[runnervm3jyl0:48848] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffab88a5a6f]
[runnervm3jyl0:48848] [ 8] plumed(+0x13209)[0x556bdec9e209]
[runnervm3jyl0:48848] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffab842a1ca]
[runnervm3jyl0:48848] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffab842a28b]
[runnervm3jyl0:48848] [11] plumed(+0x134a5)[0x556bdec9e4a5]
[runnervm3jyl0:48848] *** End of error message ***
</pre>
{% endraw %}
