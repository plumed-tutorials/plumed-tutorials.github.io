Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1548) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az1690-151:05431] *** Process received signal ***
[fv-az1690-151:05431] Signal: Aborted (6)
[fv-az1690-151:05431] Signal code:  (-6)
[fv-az1690-151:05431] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb14d445330]
[fv-az1690-151:05431] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb14d49eb2c]
[fv-az1690-151:05431] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb14d44527e]
[fv-az1690-151:05431] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb14d4288ff]
[fv-az1690-151:05431] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb14d8a5ff5]
[fv-az1690-151:05431] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb14d8bb0da]
[fv-az1690-151:05431] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb14d8a5a55]
[fv-az1690-151:05431] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb14d8a5a6f]
[fv-az1690-151:05431] [ 8] plumed_master(+0x146dd)[0x561e0c4666dd]
[fv-az1690-151:05431] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb14d42a1ca]
[fv-az1690-151:05431] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb14d42a28b]
[fv-az1690-151:05431] [11] plumed_master(+0x15365)[0x561e0c467365]
[fv-az1690-151:05431] *** End of error message ***
</pre>
{% endraw %}
