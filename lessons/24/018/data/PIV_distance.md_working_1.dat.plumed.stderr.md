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
[fv-az1690-151:05416] *** Process received signal ***
[fv-az1690-151:05416] Signal: Aborted (6)
[fv-az1690-151:05416] Signal code:  (-6)
[fv-az1690-151:05416] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd5c4e45330]
[fv-az1690-151:05416] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd5c4e9eb2c]
[fv-az1690-151:05416] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd5c4e4527e]
[fv-az1690-151:05416] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd5c4e288ff]
[fv-az1690-151:05416] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd5c52a5ff5]
[fv-az1690-151:05416] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd5c52bb0da]
[fv-az1690-151:05416] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd5c52a5a55]
[fv-az1690-151:05416] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd5c52a5a6f]
[fv-az1690-151:05416] [ 8] plumed(+0x13209)[0x557854610209]
[fv-az1690-151:05416] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd5c4e2a1ca]
[fv-az1690-151:05416] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd5c4e2a28b]
[fv-az1690-151:05416] [11] plumed(+0x134a5)[0x5578546104a5]
[fv-az1690-151:05416] *** End of error message ***
</pre>
{% endraw %}
