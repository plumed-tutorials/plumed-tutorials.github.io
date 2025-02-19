Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1548) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1690-151:05521] *** Process received signal ***
[fv-az1690-151:05521] Signal: Aborted (6)
[fv-az1690-151:05521] Signal code:  (-6)
[fv-az1690-151:05521] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feeef045330]
[fv-az1690-151:05521] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feeef09eb2c]
[fv-az1690-151:05521] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feeef04527e]
[fv-az1690-151:05521] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feeef0288ff]
[fv-az1690-151:05521] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feeef4a5ff5]
[fv-az1690-151:05521] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feeef4bb0da]
[fv-az1690-151:05521] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feeef4a5a55]
[fv-az1690-151:05521] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feeef4a5a6f]
[fv-az1690-151:05521] [ 8] plumed_master(+0x146dd)[0x55aaace516dd]
[fv-az1690-151:05521] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feeef02a1ca]
[fv-az1690-151:05521] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feeef02a28b]
[fv-az1690-151:05521] [11] plumed_master(+0x15365)[0x55aaace52365]
[fv-az1690-151:05521] *** End of error message ***
</pre>
{% endraw %}
