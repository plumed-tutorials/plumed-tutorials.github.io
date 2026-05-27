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
[runnervm3jyl0:78956] *** Process received signal ***
[runnervm3jyl0:78956] Signal: Aborted (6)
[runnervm3jyl0:78956] Signal code:  (-6)
[runnervm3jyl0:78956] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9a11445330]
[runnervm3jyl0:78956] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9a1149eb2c]
[runnervm3jyl0:78956] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9a1144527e]
[runnervm3jyl0:78956] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9a114288ff]
[runnervm3jyl0:78956] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9a118a5ff5]
[runnervm3jyl0:78956] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9a118bb0da]
[runnervm3jyl0:78956] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9a118a5a55]
[runnervm3jyl0:78956] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9a118a5a6f]
[runnervm3jyl0:78956] [ 8] plumed(+0x13209)[0x563dcd388209]
[runnervm3jyl0:78956] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9a1142a1ca]
[runnervm3jyl0:78956] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9a1142a28b]
[runnervm3jyl0:78956] [11] plumed(+0x134a5)[0x563dcd3884a5]
[runnervm3jyl0:78956] *** End of error message ***
</pre>
{% endraw %}
