Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1542) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[runnervm3jyl0:47062] *** Process received signal ***
[runnervm3jyl0:47062] Signal: Aborted (6)
[runnervm3jyl0:47062] Signal code:  (-6)
[runnervm3jyl0:47062] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdb85a45330]
[runnervm3jyl0:47062] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdb85a9eb2c]
[runnervm3jyl0:47062] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdb85a4527e]
[runnervm3jyl0:47062] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdb85a288ff]
[runnervm3jyl0:47062] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdb85ea5ff5]
[runnervm3jyl0:47062] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdb85ebb0da]
[runnervm3jyl0:47062] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdb85ea5a55]
[runnervm3jyl0:47062] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdb85ea5a6f]
[runnervm3jyl0:47062] [ 8] plumed_master(+0x146dd)[0x559eb2f186dd]
[runnervm3jyl0:47062] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdb85a2a1ca]
[runnervm3jyl0:47062] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdb85a2a28b]
[runnervm3jyl0:47062] [11] plumed_master(+0x15365)[0x559eb2f19365]
[runnervm3jyl0:47062] *** End of error message ***
</pre>
{% endraw %}
