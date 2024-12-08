Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1334) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1778-96:04016] *** Process received signal ***
[fv-az1778-96:04016] Signal: Aborted (6)
[fv-az1778-96:04016] Signal code:  (-6)
[fv-az1778-96:04016] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f17c2642520]
[fv-az1778-96:04016] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f17c26969fc]
[fv-az1778-96:04016] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f17c2642476]
[fv-az1778-96:04016] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f17c26287f3]
[fv-az1778-96:04016] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f17c2aa2b9e]
[fv-az1778-96:04016] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f17c2aae20c]
[fv-az1778-96:04016] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f17c2aae277]
[fv-az1778-96:04016] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f17c2aae52b]
[fv-az1778-96:04016] [ 8] plumed_master(+0x14254)[0x5603122e2254]
[fv-az1778-96:04016] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f17c2629d90]
[fv-az1778-96:04016] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f17c2629e40]
[fv-az1778-96:04016] [11] plumed_master(+0x14eb5)[0x5603122e2eb5]
[fv-az1778-96:04016] *** End of error message ***
</pre>
{% endraw %}
