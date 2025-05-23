Stderr for source:  examples.md_working_1.dat   
Download: [zipped raw stdout](examples.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/DLLoader.cpp:50) void* PLMD::DLLoader::load(const std::string&)
Could not load library /path/to/PythonCVInterface.so
/path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[pkrvmf6wy0o8zjz:58965] *** Process received signal ***
[pkrvmf6wy0o8zjz:58965] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58965] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58965] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3b03245330]
[pkrvmf6wy0o8zjz:58965] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3b0329eb2c]
[pkrvmf6wy0o8zjz:58965] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3b0324527e]
[pkrvmf6wy0o8zjz:58965] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3b032288ff]
[pkrvmf6wy0o8zjz:58965] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3b036a5ff5]
[pkrvmf6wy0o8zjz:58965] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3b036bb0da]
[pkrvmf6wy0o8zjz:58965] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3b036a5a55]
[pkrvmf6wy0o8zjz:58965] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3b036a5a6f]
[pkrvmf6wy0o8zjz:58965] [ 8] plumed_master(+0x146dd)[0x555a155b06dd]
[pkrvmf6wy0o8zjz:58965] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3b0322a1ca]
[pkrvmf6wy0o8zjz:58965] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3b0322a28b]
[pkrvmf6wy0o8zjz:58965] [11] plumed_master(+0x15365)[0x555a155b1365]
[pkrvmf6wy0o8zjz:58965] *** End of error message ***
</pre>
{% endraw %}
