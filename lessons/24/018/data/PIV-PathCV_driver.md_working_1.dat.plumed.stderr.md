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
[runnervm3jyl0:79017] *** Process received signal ***
[runnervm3jyl0:79017] Signal: Aborted (6)
[runnervm3jyl0:79017] Signal code:  (-6)
[runnervm3jyl0:79017] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f22f9245330]
[runnervm3jyl0:79017] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f22f929eb2c]
[runnervm3jyl0:79017] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f22f924527e]
[runnervm3jyl0:79017] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f22f92288ff]
[runnervm3jyl0:79017] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f22f96a5ff5]
[runnervm3jyl0:79017] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f22f96bb0da]
[runnervm3jyl0:79017] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f22f96a5a55]
[runnervm3jyl0:79017] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f22f96a5a6f]
[runnervm3jyl0:79017] [ 8] plumed(+0x13209)[0x5630357a2209]
[runnervm3jyl0:79017] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f22f922a1ca]
[runnervm3jyl0:79017] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f22f922a28b]
[runnervm3jyl0:79017] [11] plumed(+0x134a5)[0x5630357a24a5]
[runnervm3jyl0:79017] *** End of error message ***
</pre>
{% endraw %}
