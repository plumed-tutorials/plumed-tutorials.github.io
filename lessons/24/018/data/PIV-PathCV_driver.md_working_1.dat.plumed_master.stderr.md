Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1551) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmbietmlfzoi:34780] *** Process received signal ***
[pkrvmbietmlfzoi:34780] Signal: Aborted (6)
[pkrvmbietmlfzoi:34780] Signal code:  (-6)
[pkrvmbietmlfzoi:34780] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4fe5a45330]
[pkrvmbietmlfzoi:34780] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4fe5a9eb2c]
[pkrvmbietmlfzoi:34780] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4fe5a4527e]
[pkrvmbietmlfzoi:34780] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4fe5a288ff]
[pkrvmbietmlfzoi:34780] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4fe5ea5ff5]
[pkrvmbietmlfzoi:34780] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4fe5ebb0da]
[pkrvmbietmlfzoi:34780] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4fe5ea5a55]
[pkrvmbietmlfzoi:34780] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4fe5ea5a6f]
[pkrvmbietmlfzoi:34780] [ 8] plumed_master(+0x146dd)[0x55ecdffaf6dd]
[pkrvmbietmlfzoi:34780] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4fe5a2a1ca]
[pkrvmbietmlfzoi:34780] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4fe5a2a28b]
[pkrvmbietmlfzoi:34780] [11] plumed_master(+0x15365)[0x55ecdffb0365]
[pkrvmbietmlfzoi:34780] *** End of error message ***
</pre>
{% endraw %}
