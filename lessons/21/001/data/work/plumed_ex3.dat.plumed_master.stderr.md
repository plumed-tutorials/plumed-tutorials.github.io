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
[pkrvmf6wy0o8zjz:60548] *** Process received signal ***
[pkrvmf6wy0o8zjz:60548] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60548] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60548] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8848845330]
[pkrvmf6wy0o8zjz:60548] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f884889eb2c]
[pkrvmf6wy0o8zjz:60548] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f884884527e]
[pkrvmf6wy0o8zjz:60548] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f88488288ff]
[pkrvmf6wy0o8zjz:60548] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8848ca5ff5]
[pkrvmf6wy0o8zjz:60548] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8848cbb0da]
[pkrvmf6wy0o8zjz:60548] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8848ca5a55]
[pkrvmf6wy0o8zjz:60548] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8848ca5a6f]
[pkrvmf6wy0o8zjz:60548] [ 8] plumed_master(+0x146dd)[0x55e9792ab6dd]
[pkrvmf6wy0o8zjz:60548] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f884882a1ca]
[pkrvmf6wy0o8zjz:60548] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f884882a28b]
[pkrvmf6wy0o8zjz:60548] [11] plumed_master(+0x15365)[0x55e9792ac365]
[pkrvmf6wy0o8zjz:60548] *** End of error message ***
</pre>
{% endraw %}
