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
[pkrvmbietmlfzoi:36039] *** Process received signal ***
[pkrvmbietmlfzoi:36039] Signal: Aborted (6)
[pkrvmbietmlfzoi:36039] Signal code:  (-6)
[pkrvmbietmlfzoi:36039] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4dc1a45330]
[pkrvmbietmlfzoi:36039] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4dc1a9eb2c]
[pkrvmbietmlfzoi:36039] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4dc1a4527e]
[pkrvmbietmlfzoi:36039] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4dc1a288ff]
[pkrvmbietmlfzoi:36039] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4dc1ea5ff5]
[pkrvmbietmlfzoi:36039] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4dc1ebb0da]
[pkrvmbietmlfzoi:36039] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4dc1ea5a55]
[pkrvmbietmlfzoi:36039] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4dc1ea5a6f]
[pkrvmbietmlfzoi:36039] [ 8] plumed_master(+0x146dd)[0x55fc75b826dd]
[pkrvmbietmlfzoi:36039] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4dc1a2a1ca]
[pkrvmbietmlfzoi:36039] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4dc1a2a28b]
[pkrvmbietmlfzoi:36039] [11] plumed_master(+0x15365)[0x55fc75b83365]
[pkrvmbietmlfzoi:36039] *** End of error message ***
</pre>
{% endraw %}
