Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1102) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1778-96:04008] *** Process received signal ***
[fv-az1778-96:04008] Signal: Aborted (6)
[fv-az1778-96:04008] Signal code:  (-6)
[fv-az1778-96:04008] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6faee42520]
[fv-az1778-96:04008] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6faee969fc]
[fv-az1778-96:04008] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6faee42476]
[fv-az1778-96:04008] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6faee287f3]
[fv-az1778-96:04008] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6faf2a2b9e]
[fv-az1778-96:04008] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6faf2ae20c]
[fv-az1778-96:04008] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6faf2ae277]
[fv-az1778-96:04008] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6faf2ae52b]
[fv-az1778-96:04008] [ 8] plumed(+0x12f48)[0x560bef65ef48]
[fv-az1778-96:04008] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6faee29d90]
[fv-az1778-96:04008] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6faee29e40]
[fv-az1778-96:04008] [11] plumed(+0x131e5)[0x560bef65f1e5]
[fv-az1778-96:04008] *** End of error message ***
</pre>
{% endraw %}
