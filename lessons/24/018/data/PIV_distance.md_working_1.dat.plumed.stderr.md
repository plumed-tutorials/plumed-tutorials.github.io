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
[pkrvmf6wy0o8zjz:58935] *** Process received signal ***
[pkrvmf6wy0o8zjz:58935] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58935] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58935] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcd71645330]
[pkrvmf6wy0o8zjz:58935] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcd7169eb2c]
[pkrvmf6wy0o8zjz:58935] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcd7164527e]
[pkrvmf6wy0o8zjz:58935] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcd716288ff]
[pkrvmf6wy0o8zjz:58935] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcd71aa5ff5]
[pkrvmf6wy0o8zjz:58935] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcd71abb0da]
[pkrvmf6wy0o8zjz:58935] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcd71aa5a55]
[pkrvmf6wy0o8zjz:58935] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcd71aa5a6f]
[pkrvmf6wy0o8zjz:58935] [ 8] plumed(+0x13209)[0x55f317e52209]
[pkrvmf6wy0o8zjz:58935] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcd7162a1ca]
[pkrvmf6wy0o8zjz:58935] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcd7162a28b]
[pkrvmf6wy0o8zjz:58935] [11] plumed(+0x134a5)[0x55f317e524a5]
[pkrvmf6wy0o8zjz:58935] *** End of error message ***
</pre>
{% endraw %}
