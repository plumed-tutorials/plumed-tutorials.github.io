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
[fv-az2211-783:05466] *** Process received signal ***
[fv-az2211-783:05466] Signal: Aborted (6)
[fv-az2211-783:05466] Signal code:  (-6)
[fv-az2211-783:05466] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb6bd445330]
[fv-az2211-783:05466] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb6bd49eb2c]
[fv-az2211-783:05466] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb6bd44527e]
[fv-az2211-783:05466] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb6bd4288ff]
[fv-az2211-783:05466] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb6bd8a5ff5]
[fv-az2211-783:05466] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb6bd8bb0da]
[fv-az2211-783:05466] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb6bd8a5a55]
[fv-az2211-783:05466] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb6bd8a5a6f]
[fv-az2211-783:05466] [ 8] plumed_master(+0x146dd)[0x55efccfd56dd]
[fv-az2211-783:05466] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb6bd42a1ca]
[fv-az2211-783:05466] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb6bd42a28b]
[fv-az2211-783:05466] [11] plumed_master(+0x15365)[0x55efccfd6365]
[fv-az2211-783:05466] *** End of error message ***
</pre>
{% endraw %}
