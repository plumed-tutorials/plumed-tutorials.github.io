Stderr for source:  PIV_distance.md_working_1.dat   
Download: [zipped raw stdout](PIV_distance.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV_distance.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1551) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmf6wy0o8zjz:58673] *** Process received signal ***
[pkrvmf6wy0o8zjz:58673] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58673] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58673] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb916e45330]
[pkrvmf6wy0o8zjz:58673] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb916e9eb2c]
[pkrvmf6wy0o8zjz:58673] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb916e4527e]
[pkrvmf6wy0o8zjz:58673] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb916e288ff]
[pkrvmf6wy0o8zjz:58673] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb9172a5ff5]
[pkrvmf6wy0o8zjz:58673] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb9172bb0da]
[pkrvmf6wy0o8zjz:58673] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb9172a5a55]
[pkrvmf6wy0o8zjz:58673] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb9172a5a6f]
[pkrvmf6wy0o8zjz:58673] [ 8] plumed_master(+0x146dd)[0x55869de736dd]
[pkrvmf6wy0o8zjz:58673] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb916e2a1ca]
[pkrvmf6wy0o8zjz:58673] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb916e2a28b]
[pkrvmf6wy0o8zjz:58673] [11] plumed_master(+0x15365)[0x55869de74365]
[pkrvmf6wy0o8zjz:58673] *** End of error message ***
</pre>
{% endraw %}
