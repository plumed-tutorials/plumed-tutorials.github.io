Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervm3jyl0:48773] *** Process received signal ***
[runnervm3jyl0:48773] Signal: Aborted (6)
[runnervm3jyl0:48773] Signal code:  (-6)
[runnervm3jyl0:48773] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1bef245330]
[runnervm3jyl0:48773] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1bef29eb2c]
[runnervm3jyl0:48773] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1bef24527e]
[runnervm3jyl0:48773] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1bef2288ff]
[runnervm3jyl0:48773] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1bef6a5ff5]
[runnervm3jyl0:48773] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1bef6bb0da]
[runnervm3jyl0:48773] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1bef6a5a55]
[runnervm3jyl0:48773] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1bef6a5a6f]
[runnervm3jyl0:48773] [ 8] plumed(+0x13209)[0x55f217265209]
[runnervm3jyl0:48773] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1bef22a1ca]
[runnervm3jyl0:48773] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1bef22a28b]
[runnervm3jyl0:48773] [11] plumed(+0x134a5)[0x55f2172654a5]
[runnervm3jyl0:48773] *** End of error message ***
</pre>
{% endraw %}
