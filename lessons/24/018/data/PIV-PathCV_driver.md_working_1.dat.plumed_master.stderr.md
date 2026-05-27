Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1542) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[runnervm3jyl0:79033] *** Process received signal ***
[runnervm3jyl0:79033] Signal: Aborted (6)
[runnervm3jyl0:79033] Signal code:  (-6)
[runnervm3jyl0:79033] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f393c845330]
[runnervm3jyl0:79033] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f393c89eb2c]
[runnervm3jyl0:79033] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f393c84527e]
[runnervm3jyl0:79033] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f393c8288ff]
[runnervm3jyl0:79033] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f393cca5ff5]
[runnervm3jyl0:79033] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f393ccbb0da]
[runnervm3jyl0:79033] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f393cca5a55]
[runnervm3jyl0:79033] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f393cca5a6f]
[runnervm3jyl0:79033] [ 8] plumed_master(+0x146dd)[0x5568d86756dd]
[runnervm3jyl0:79033] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f393c82a1ca]
[runnervm3jyl0:79033] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f393c82a28b]
[runnervm3jyl0:79033] [11] plumed_master(+0x15365)[0x5568d8676365]
[runnervm3jyl0:79033] *** End of error message ***
</pre>
{% endraw %}
