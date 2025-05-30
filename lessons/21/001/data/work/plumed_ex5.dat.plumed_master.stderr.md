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
[pkrvmf6wy0o8zjz:60454] *** Process received signal ***
[pkrvmf6wy0o8zjz:60454] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60454] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60454] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f51cf845330]
[pkrvmf6wy0o8zjz:60454] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f51cf89eb2c]
[pkrvmf6wy0o8zjz:60454] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f51cf84527e]
[pkrvmf6wy0o8zjz:60454] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f51cf8288ff]
[pkrvmf6wy0o8zjz:60454] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f51cfca5ff5]
[pkrvmf6wy0o8zjz:60454] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f51cfcbb0da]
[pkrvmf6wy0o8zjz:60454] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f51cfca5a55]
[pkrvmf6wy0o8zjz:60454] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f51cfca5a6f]
[pkrvmf6wy0o8zjz:60454] [ 8] plumed_master(+0x146dd)[0x557ecd1f26dd]
[pkrvmf6wy0o8zjz:60454] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f51cf82a1ca]
[pkrvmf6wy0o8zjz:60454] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f51cf82a28b]
[pkrvmf6wy0o8zjz:60454] [11] plumed_master(+0x15365)[0x557ecd1f3365]
[pkrvmf6wy0o8zjz:60454] *** End of error message ***
</pre>
{% endraw %}
