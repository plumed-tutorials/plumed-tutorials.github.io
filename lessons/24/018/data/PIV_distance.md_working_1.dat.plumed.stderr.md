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
[pkrvmf6wy0o8zjz:58657] *** Process received signal ***
[pkrvmf6wy0o8zjz:58657] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58657] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58657] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4c42245330]
[pkrvmf6wy0o8zjz:58657] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4c4229eb2c]
[pkrvmf6wy0o8zjz:58657] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4c4224527e]
[pkrvmf6wy0o8zjz:58657] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4c422288ff]
[pkrvmf6wy0o8zjz:58657] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4c426a5ff5]
[pkrvmf6wy0o8zjz:58657] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4c426bb0da]
[pkrvmf6wy0o8zjz:58657] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4c426a5a55]
[pkrvmf6wy0o8zjz:58657] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4c426a5a6f]
[pkrvmf6wy0o8zjz:58657] [ 8] plumed(+0x13209)[0x55bd145b8209]
[pkrvmf6wy0o8zjz:58657] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4c4222a1ca]
[pkrvmf6wy0o8zjz:58657] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4c4222a28b]
[pkrvmf6wy0o8zjz:58657] [11] plumed(+0x134a5)[0x55bd145b84a5]
[pkrvmf6wy0o8zjz:58657] *** End of error message ***
</pre>
{% endraw %}
