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
[pkrvmbietmlfzoi:36113] *** Process received signal ***
[pkrvmbietmlfzoi:36113] Signal: Aborted (6)
[pkrvmbietmlfzoi:36113] Signal code:  (-6)
[pkrvmbietmlfzoi:36113] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa633445330]
[pkrvmbietmlfzoi:36113] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa63349eb2c]
[pkrvmbietmlfzoi:36113] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa63344527e]
[pkrvmbietmlfzoi:36113] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa6334288ff]
[pkrvmbietmlfzoi:36113] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa6338a5ff5]
[pkrvmbietmlfzoi:36113] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa6338bb0da]
[pkrvmbietmlfzoi:36113] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa6338a5a55]
[pkrvmbietmlfzoi:36113] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa6338a5a6f]
[pkrvmbietmlfzoi:36113] [ 8] plumed_master(+0x146dd)[0x55677a4856dd]
[pkrvmbietmlfzoi:36113] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa63342a1ca]
[pkrvmbietmlfzoi:36113] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa63342a28b]
[pkrvmbietmlfzoi:36113] [11] plumed_master(+0x15365)[0x55677a486365]
[pkrvmbietmlfzoi:36113] *** End of error message ***
</pre>
{% endraw %}
