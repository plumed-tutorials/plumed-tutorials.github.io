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
[runnervm3jyl0:47103] *** Process received signal ***
[runnervm3jyl0:47103] Signal: Aborted (6)
[runnervm3jyl0:47103] Signal code:  (-6)
[runnervm3jyl0:47103] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa8b3245330]
[runnervm3jyl0:47103] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa8b329eb2c]
[runnervm3jyl0:47103] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa8b324527e]
[runnervm3jyl0:47103] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa8b32288ff]
[runnervm3jyl0:47103] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa8b36a5ff5]
[runnervm3jyl0:47103] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa8b36bb0da]
[runnervm3jyl0:47103] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa8b36a5a55]
[runnervm3jyl0:47103] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa8b36a5a6f]
[runnervm3jyl0:47103] [ 8] plumed(+0x13209)[0x55d18b526209]
[runnervm3jyl0:47103] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa8b322a1ca]
[runnervm3jyl0:47103] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa8b322a28b]
[runnervm3jyl0:47103] [11] plumed(+0x134a5)[0x55d18b5264a5]
[runnervm3jyl0:47103] *** End of error message ***
</pre>
{% endraw %}
