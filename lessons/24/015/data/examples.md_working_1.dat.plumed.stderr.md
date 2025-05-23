Stderr for source:  examples.md_working_1.dat   
Download: [zipped raw stdout](examples.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1227) void PLMD::PlumedMain::load(const std::string&)
I cannot load library /path/to/PythonCVInterface.so /path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[pkrvmf6wy0o8zjz:58949] *** Process received signal ***
[pkrvmf6wy0o8zjz:58949] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58949] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58949] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb841245330]
[pkrvmf6wy0o8zjz:58949] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb84129eb2c]
[pkrvmf6wy0o8zjz:58949] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb84124527e]
[pkrvmf6wy0o8zjz:58949] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb8412288ff]
[pkrvmf6wy0o8zjz:58949] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb8416a5ff5]
[pkrvmf6wy0o8zjz:58949] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb8416bb0da]
[pkrvmf6wy0o8zjz:58949] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb8416a5a55]
[pkrvmf6wy0o8zjz:58949] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb8416a5a6f]
[pkrvmf6wy0o8zjz:58949] [ 8] plumed(+0x13209)[0x55b0a55f1209]
[pkrvmf6wy0o8zjz:58949] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb84122a1ca]
[pkrvmf6wy0o8zjz:58949] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb84122a28b]
[pkrvmf6wy0o8zjz:58949] [11] plumed(+0x134a5)[0x55b0a55f14a5]
[pkrvmf6wy0o8zjz:58949] *** End of error message ***
</pre>
{% endraw %}
