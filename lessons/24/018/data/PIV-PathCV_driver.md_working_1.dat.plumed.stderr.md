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
[fv-az2211-783:05544] *** Process received signal ***
[fv-az2211-783:05544] Signal: Aborted (6)
[fv-az2211-783:05544] Signal code:  (-6)
[fv-az2211-783:05544] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdc9e245330]
[fv-az2211-783:05544] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdc9e29eb2c]
[fv-az2211-783:05544] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdc9e24527e]
[fv-az2211-783:05544] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdc9e2288ff]
[fv-az2211-783:05544] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdc9e6a5ff5]
[fv-az2211-783:05544] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdc9e6bb0da]
[fv-az2211-783:05544] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdc9e6a5a55]
[fv-az2211-783:05544] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdc9e6a5a6f]
[fv-az2211-783:05544] [ 8] plumed(+0x13209)[0x557b39acb209]
[fv-az2211-783:05544] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdc9e22a1ca]
[fv-az2211-783:05544] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdc9e22a28b]
[fv-az2211-783:05544] [11] plumed(+0x134a5)[0x557b39acb4a5]
[fv-az2211-783:05544] *** End of error message ***
</pre>
{% endraw %}
