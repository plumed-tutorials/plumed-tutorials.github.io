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
[pkrvmf6wy0o8zjz:58908] *** Process received signal ***
[pkrvmf6wy0o8zjz:58908] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58908] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58908] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa3ecc45330]
[pkrvmf6wy0o8zjz:58908] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa3ecc9eb2c]
[pkrvmf6wy0o8zjz:58908] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa3ecc4527e]
[pkrvmf6wy0o8zjz:58908] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa3ecc288ff]
[pkrvmf6wy0o8zjz:58908] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa3ed0a5ff5]
[pkrvmf6wy0o8zjz:58908] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa3ed0bb0da]
[pkrvmf6wy0o8zjz:58908] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa3ed0a5a55]
[pkrvmf6wy0o8zjz:58908] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa3ed0a5a6f]
[pkrvmf6wy0o8zjz:58908] [ 8] plumed(+0x13209)[0x55a80d8b7209]
[pkrvmf6wy0o8zjz:58908] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa3ecc2a1ca]
[pkrvmf6wy0o8zjz:58908] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa3ecc2a28b]
[pkrvmf6wy0o8zjz:58908] [11] plumed(+0x134a5)[0x55a80d8b74a5]
[pkrvmf6wy0o8zjz:58908] *** End of error message ***
</pre>
{% endraw %}
