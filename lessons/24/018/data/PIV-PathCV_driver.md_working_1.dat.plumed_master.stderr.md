Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1334) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1778-96:04070] *** Process received signal ***
[fv-az1778-96:04070] Signal: Aborted (6)
[fv-az1778-96:04070] Signal code:  (-6)
[fv-az1778-96:04070] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fae3d842520]
[fv-az1778-96:04070] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fae3d8969fc]
[fv-az1778-96:04070] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fae3d842476]
[fv-az1778-96:04070] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fae3d8287f3]
[fv-az1778-96:04070] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fae3dca2b9e]
[fv-az1778-96:04070] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fae3dcae20c]
[fv-az1778-96:04070] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fae3dcae277]
[fv-az1778-96:04070] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fae3dcae52b]
[fv-az1778-96:04070] [ 8] plumed_master(+0x14254)[0x55d61fc15254]
[fv-az1778-96:04070] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fae3d829d90]
[fv-az1778-96:04070] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fae3d829e40]
[fv-az1778-96:04070] [11] plumed_master(+0x14eb5)[0x55d61fc15eb5]
[fv-az1778-96:04070] *** End of error message ***
</pre>
{% endraw %}
