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
[pkrvmf6wy0o8zjz:58999] *** Process received signal ***
[pkrvmf6wy0o8zjz:58999] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58999] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58999] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8a97445330]
[pkrvmf6wy0o8zjz:58999] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8a9749eb2c]
[pkrvmf6wy0o8zjz:58999] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8a9744527e]
[pkrvmf6wy0o8zjz:58999] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8a974288ff]
[pkrvmf6wy0o8zjz:58999] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8a978a5ff5]
[pkrvmf6wy0o8zjz:58999] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8a978bb0da]
[pkrvmf6wy0o8zjz:58999] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8a978a5a55]
[pkrvmf6wy0o8zjz:58999] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8a978a5a6f]
[pkrvmf6wy0o8zjz:58999] [ 8] plumed(+0x13209)[0x55b4ba3d5209]
[pkrvmf6wy0o8zjz:58999] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8a9742a1ca]
[pkrvmf6wy0o8zjz:58999] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8a9742a28b]
[pkrvmf6wy0o8zjz:58999] [11] plumed(+0x134a5)[0x55b4ba3d54a5]
[pkrvmf6wy0o8zjz:58999] *** End of error message ***
</pre>
{% endraw %}
