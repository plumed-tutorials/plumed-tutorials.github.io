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
[pkrvmbietmlfzoi:36091] *** Process received signal ***
[pkrvmbietmlfzoi:36091] Signal: Aborted (6)
[pkrvmbietmlfzoi:36091] Signal code:  (-6)
[pkrvmbietmlfzoi:36091] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fed82c45330]
[pkrvmbietmlfzoi:36091] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fed82c9eb2c]
[pkrvmbietmlfzoi:36091] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fed82c4527e]
[pkrvmbietmlfzoi:36091] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fed82c288ff]
[pkrvmbietmlfzoi:36091] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fed830a5ff5]
[pkrvmbietmlfzoi:36091] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fed830bb0da]
[pkrvmbietmlfzoi:36091] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fed830a5a55]
[pkrvmbietmlfzoi:36091] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fed830a5a6f]
[pkrvmbietmlfzoi:36091] [ 8] plumed(+0x13209)[0x55cd71dea209]
[pkrvmbietmlfzoi:36091] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fed82c2a1ca]
[pkrvmbietmlfzoi:36091] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fed82c2a28b]
[pkrvmbietmlfzoi:36091] [11] plumed(+0x134a5)[0x55cd71dea4a5]
[pkrvmbietmlfzoi:36091] *** End of error message ***
</pre>
{% endraw %}
