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
[runnervm3jyl0:78971] *** Process received signal ***
[runnervm3jyl0:78971] Signal: Aborted (6)
[runnervm3jyl0:78971] Signal code:  (-6)
[runnervm3jyl0:78971] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdda8a45330]
[runnervm3jyl0:78971] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdda8a9eb2c]
[runnervm3jyl0:78971] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdda8a4527e]
[runnervm3jyl0:78971] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdda8a288ff]
[runnervm3jyl0:78971] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdda8ea5ff5]
[runnervm3jyl0:78971] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdda8ebb0da]
[runnervm3jyl0:78971] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdda8ea5a55]
[runnervm3jyl0:78971] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdda8ea5a6f]
[runnervm3jyl0:78971] [ 8] plumed_master(+0x146dd)[0x55da619036dd]
[runnervm3jyl0:78971] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdda8a2a1ca]
[runnervm3jyl0:78971] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdda8a2a28b]
[runnervm3jyl0:78971] [11] plumed_master(+0x15365)[0x55da61904365]
[runnervm3jyl0:78971] *** End of error message ***
</pre>
{% endraw %}
