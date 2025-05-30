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
[pkrvmf6wy0o8zjz:60356] *** Process received signal ***
[pkrvmf6wy0o8zjz:60356] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60356] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60356] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5374445330]
[pkrvmf6wy0o8zjz:60356] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f537449eb2c]
[pkrvmf6wy0o8zjz:60356] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f537444527e]
[pkrvmf6wy0o8zjz:60356] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f53744288ff]
[pkrvmf6wy0o8zjz:60356] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f53748a5ff5]
[pkrvmf6wy0o8zjz:60356] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f53748bb0da]
[pkrvmf6wy0o8zjz:60356] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f53748a5a55]
[pkrvmf6wy0o8zjz:60356] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f53748a5a6f]
[pkrvmf6wy0o8zjz:60356] [ 8] plumed(+0x13209)[0x55e9d183e209]
[pkrvmf6wy0o8zjz:60356] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f537442a1ca]
[pkrvmf6wy0o8zjz:60356] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f537442a28b]
[pkrvmf6wy0o8zjz:60356] [11] plumed(+0x134a5)[0x55e9d183e4a5]
[pkrvmf6wy0o8zjz:60356] *** End of error message ***
</pre>
{% endraw %}
