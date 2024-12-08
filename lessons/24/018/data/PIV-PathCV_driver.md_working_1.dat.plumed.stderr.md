Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1102) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1778-96:04062] *** Process received signal ***
[fv-az1778-96:04062] Signal: Aborted (6)
[fv-az1778-96:04062] Signal code:  (-6)
[fv-az1778-96:04062] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1105042520]
[fv-az1778-96:04062] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f11050969fc]
[fv-az1778-96:04062] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1105042476]
[fv-az1778-96:04062] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f11050287f3]
[fv-az1778-96:04062] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f11054a2b9e]
[fv-az1778-96:04062] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f11054ae20c]
[fv-az1778-96:04062] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f11054ae277]
[fv-az1778-96:04062] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f11054ae52b]
[fv-az1778-96:04062] [ 8] plumed(+0x12f48)[0x5569e9b3cf48]
[fv-az1778-96:04062] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1105029d90]
[fv-az1778-96:04062] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1105029e40]
[fv-az1778-96:04062] [11] plumed(+0x131e5)[0x5569e9b3d1e5]
[fv-az1778-96:04062] *** End of error message ***
</pre>
{% endraw %}
