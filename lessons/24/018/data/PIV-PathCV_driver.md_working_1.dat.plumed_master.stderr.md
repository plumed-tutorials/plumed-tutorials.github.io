Stderr for source:  PIV-PathCV_driver.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1551) FILE* PLMD::PlumedMain::fopen(const char*, const char*)
+++ assertion failed: fp
file Liq.pdb cannot be found
[pkrvmf6wy0o8zjz:59016] *** Process received signal ***
[pkrvmf6wy0o8zjz:59016] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59016] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59016] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8d55a45330]
[pkrvmf6wy0o8zjz:59016] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8d55a9eb2c]
[pkrvmf6wy0o8zjz:59016] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8d55a4527e]
[pkrvmf6wy0o8zjz:59016] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8d55a288ff]
[pkrvmf6wy0o8zjz:59016] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8d55ea5ff5]
[pkrvmf6wy0o8zjz:59016] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8d55ebb0da]
[pkrvmf6wy0o8zjz:59016] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8d55ea5a55]
[pkrvmf6wy0o8zjz:59016] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8d55ea5a6f]
[pkrvmf6wy0o8zjz:59016] [ 8] plumed_master(+0x146dd)[0x55c8e01e96dd]
[pkrvmf6wy0o8zjz:59016] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8d55a2a1ca]
[pkrvmf6wy0o8zjz:59016] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8d55a2a28b]
[pkrvmf6wy0o8zjz:59016] [11] plumed_master(+0x15365)[0x55c8e01ea365]
[pkrvmf6wy0o8zjz:59016] *** End of error message ***
</pre>
{% endraw %}
