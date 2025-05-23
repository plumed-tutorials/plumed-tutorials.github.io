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
[pkrvmf6wy0o8zjz:60604] *** Process received signal ***
[pkrvmf6wy0o8zjz:60604] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60604] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60604] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8b55645330]
[pkrvmf6wy0o8zjz:60604] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8b5569eb2c]
[pkrvmf6wy0o8zjz:60604] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8b5564527e]
[pkrvmf6wy0o8zjz:60604] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8b556288ff]
[pkrvmf6wy0o8zjz:60604] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8b55aa5ff5]
[pkrvmf6wy0o8zjz:60604] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8b55abb0da]
[pkrvmf6wy0o8zjz:60604] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8b55aa5a55]
[pkrvmf6wy0o8zjz:60604] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8b55aa5a6f]
[pkrvmf6wy0o8zjz:60604] [ 8] plumed(+0x13209)[0x55e43fcdd209]
[pkrvmf6wy0o8zjz:60604] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8b5562a1ca]
[pkrvmf6wy0o8zjz:60604] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8b5562a28b]
[pkrvmf6wy0o8zjz:60604] [11] plumed(+0x134a5)[0x55e43fcdd4a5]
[pkrvmf6wy0o8zjz:60604] *** End of error message ***
</pre>
{% endraw %}
