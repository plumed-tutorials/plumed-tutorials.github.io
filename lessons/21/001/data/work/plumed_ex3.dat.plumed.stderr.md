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
[pkrvmbietmlfzoi:36017] *** Process received signal ***
[pkrvmbietmlfzoi:36017] Signal: Aborted (6)
[pkrvmbietmlfzoi:36017] Signal code:  (-6)
[pkrvmbietmlfzoi:36017] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff669845330]
[pkrvmbietmlfzoi:36017] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff66989eb2c]
[pkrvmbietmlfzoi:36017] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff66984527e]
[pkrvmbietmlfzoi:36017] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff6698288ff]
[pkrvmbietmlfzoi:36017] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff669ca5ff5]
[pkrvmbietmlfzoi:36017] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff669cbb0da]
[pkrvmbietmlfzoi:36017] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff669ca5a55]
[pkrvmbietmlfzoi:36017] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff669ca5a6f]
[pkrvmbietmlfzoi:36017] [ 8] plumed(+0x13209)[0x55c3ee120209]
[pkrvmbietmlfzoi:36017] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff66982a1ca]
[pkrvmbietmlfzoi:36017] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff66982a28b]
[pkrvmbietmlfzoi:36017] [11] plumed(+0x134a5)[0x55c3ee1204a5]
[pkrvmbietmlfzoi:36017] *** End of error message ***
</pre>
{% endraw %}
