Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1254) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmbietmlfzoi:34765] *** Process received signal ***
[pkrvmbietmlfzoi:34765] Signal: Aborted (6)
[pkrvmbietmlfzoi:34765] Signal code:  (-6)
[pkrvmbietmlfzoi:34765] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdebbe45330]
[pkrvmbietmlfzoi:34765] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdebbe9eb2c]
[pkrvmbietmlfzoi:34765] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdebbe4527e]
[pkrvmbietmlfzoi:34765] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdebbe288ff]
[pkrvmbietmlfzoi:34765] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdebc2a5ff5]
[pkrvmbietmlfzoi:34765] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdebc2bb0da]
[pkrvmbietmlfzoi:34765] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdebc2a5a55]
[pkrvmbietmlfzoi:34765] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdebc2a5a6f]
[pkrvmbietmlfzoi:34765] [ 8] plumed(+0x13209)[0x56337cc95209]
[pkrvmbietmlfzoi:34765] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdebbe2a1ca]
[pkrvmbietmlfzoi:34765] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdebbe2a28b]
[pkrvmbietmlfzoi:34765] [11] plumed(+0x134a5)[0x56337cc954a5]
[pkrvmbietmlfzoi:34765] *** End of error message ***
</pre>
{% endraw %}
