Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1551) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmbietmlfzoi:34721] *** Process received signal ***
[pkrvmbietmlfzoi:34721] Signal: Aborted (6)
[pkrvmbietmlfzoi:34721] Signal code:  (-6)
[pkrvmbietmlfzoi:34721] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7960645330]
[pkrvmbietmlfzoi:34721] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f796069eb2c]
[pkrvmbietmlfzoi:34721] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f796064527e]
[pkrvmbietmlfzoi:34721] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f79606288ff]
[pkrvmbietmlfzoi:34721] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7960aa5ff5]
[pkrvmbietmlfzoi:34721] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7960abb0da]
[pkrvmbietmlfzoi:34721] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7960aa5a55]
[pkrvmbietmlfzoi:34721] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7960aa5a6f]
[pkrvmbietmlfzoi:34721] [ 8] plumed_master(+0x146dd)[0x56172ab946dd]
[pkrvmbietmlfzoi:34721] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f796062a1ca]
[pkrvmbietmlfzoi:34721] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f796062a28b]
[pkrvmbietmlfzoi:34721] [11] plumed_master(+0x15365)[0x56172ab95365]
[pkrvmbietmlfzoi:34721] *** End of error message ***
</pre>
{% endraw %}
