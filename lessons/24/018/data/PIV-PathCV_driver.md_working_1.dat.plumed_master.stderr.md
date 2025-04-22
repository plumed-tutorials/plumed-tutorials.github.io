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
[fv-az2211-783:05558] *** Process received signal ***
[fv-az2211-783:05558] Signal: Aborted (6)
[fv-az2211-783:05558] Signal code:  (-6)
[fv-az2211-783:05558] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0f4ea45330]
[fv-az2211-783:05558] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0f4ea9eb2c]
[fv-az2211-783:05558] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0f4ea4527e]
[fv-az2211-783:05558] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0f4ea288ff]
[fv-az2211-783:05558] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0f4eea5ff5]
[fv-az2211-783:05558] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0f4eebb0da]
[fv-az2211-783:05558] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0f4eea5a55]
[fv-az2211-783:05558] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0f4eea5a6f]
[fv-az2211-783:05558] [ 8] plumed_master(+0x146dd)[0x556a42d266dd]
[fv-az2211-783:05558] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0f4ea2a1ca]
[fv-az2211-783:05558] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0f4ea2a28b]
[fv-az2211-783:05558] [11] plumed_master(+0x15365)[0x556a42d27365]
[fv-az2211-783:05558] *** End of error message ***
</pre>
{% endraw %}
