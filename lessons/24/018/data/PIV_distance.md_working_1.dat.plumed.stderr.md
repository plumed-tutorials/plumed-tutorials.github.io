Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1254) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmbietmlfzoi:34705] *** Process received signal ***
[pkrvmbietmlfzoi:34705] Signal: Aborted (6)
[pkrvmbietmlfzoi:34705] Signal code:  (-6)
[pkrvmbietmlfzoi:34705] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f00b1645330]
[pkrvmbietmlfzoi:34705] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f00b169eb2c]
[pkrvmbietmlfzoi:34705] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f00b164527e]
[pkrvmbietmlfzoi:34705] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f00b16288ff]
[pkrvmbietmlfzoi:34705] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f00b1aa5ff5]
[pkrvmbietmlfzoi:34705] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f00b1abb0da]
[pkrvmbietmlfzoi:34705] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f00b1aa5a55]
[pkrvmbietmlfzoi:34705] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f00b1aa5a6f]
[pkrvmbietmlfzoi:34705] [ 8] plumed(+0x13209)[0x561090e73209]
[pkrvmbietmlfzoi:34705] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f00b162a1ca]
[pkrvmbietmlfzoi:34705] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f00b162a28b]
[pkrvmbietmlfzoi:34705] [11] plumed(+0x134a5)[0x561090e734a5]
[pkrvmbietmlfzoi:34705] *** End of error message ***
</pre>
{% endraw %}
