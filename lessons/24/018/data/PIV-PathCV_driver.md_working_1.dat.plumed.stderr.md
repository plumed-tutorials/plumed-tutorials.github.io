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
[fv-az1690-151:05505] *** Process received signal ***
[fv-az1690-151:05505] Signal: Aborted (6)
[fv-az1690-151:05505] Signal code:  (-6)
[fv-az1690-151:05505] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4ef1a45330]
[fv-az1690-151:05505] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4ef1a9eb2c]
[fv-az1690-151:05505] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4ef1a4527e]
[fv-az1690-151:05505] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4ef1a288ff]
[fv-az1690-151:05505] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4ef1ea5ff5]
[fv-az1690-151:05505] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4ef1ebb0da]
[fv-az1690-151:05505] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4ef1ea5a55]
[fv-az1690-151:05505] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4ef1ea5a6f]
[fv-az1690-151:05505] [ 8] plumed(+0x13209)[0x55fb47bdc209]
[fv-az1690-151:05505] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4ef1a2a1ca]
[fv-az1690-151:05505] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4ef1a2a28b]
[fv-az1690-151:05505] [11] plumed(+0x134a5)[0x55fb47bdc4a5]
[fv-az1690-151:05505] *** End of error message ***
</pre>
{% endraw %}
