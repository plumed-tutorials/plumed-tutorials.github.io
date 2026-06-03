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
[runnervm3jyl0:47120] *** Process received signal ***
[runnervm3jyl0:47120] Signal: Aborted (6)
[runnervm3jyl0:47120] Signal code:  (-6)
[runnervm3jyl0:47120] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5aedc45330]
[runnervm3jyl0:47120] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5aedc9eb2c]
[runnervm3jyl0:47120] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5aedc4527e]
[runnervm3jyl0:47120] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5aedc288ff]
[runnervm3jyl0:47120] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5aee0a5ff5]
[runnervm3jyl0:47120] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5aee0bb0da]
[runnervm3jyl0:47120] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5aee0a5a55]
[runnervm3jyl0:47120] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5aee0a5a6f]
[runnervm3jyl0:47120] [ 8] plumed_master(+0x146dd)[0x55f1e4bc86dd]
[runnervm3jyl0:47120] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5aedc2a1ca]
[runnervm3jyl0:47120] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5aedc2a28b]
[runnervm3jyl0:47120] [11] plumed_master(+0x15365)[0x55f1e4bc9365]
[runnervm3jyl0:47120] *** End of error message ***
</pre>
{% endraw %}
