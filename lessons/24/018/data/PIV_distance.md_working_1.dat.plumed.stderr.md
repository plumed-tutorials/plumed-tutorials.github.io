Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1254) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[fv-az2211-783:05451] *** Process received signal ***
[fv-az2211-783:05451] Signal: Aborted (6)
[fv-az2211-783:05451] Signal code:  (-6)
[fv-az2211-783:05451] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f17bea45330]
[fv-az2211-783:05451] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f17bea9eb2c]
[fv-az2211-783:05451] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f17bea4527e]
[fv-az2211-783:05451] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f17bea288ff]
[fv-az2211-783:05451] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f17beea5ff5]
[fv-az2211-783:05451] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f17beebb0da]
[fv-az2211-783:05451] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f17beea5a55]
[fv-az2211-783:05451] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f17beea5a6f]
[fv-az2211-783:05451] [ 8] plumed(+0x13209)[0x55c35d58a209]
[fv-az2211-783:05451] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f17bea2a1ca]
[fv-az2211-783:05451] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f17bea2a28b]
[fv-az2211-783:05451] [11] plumed(+0x134a5)[0x55c35d58a4a5]
[fv-az2211-783:05451] *** End of error message ***
</pre>
{% endraw %}
