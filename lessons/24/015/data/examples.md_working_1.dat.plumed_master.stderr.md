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
[runnervm3jyl0:46713] *** Process received signal ***
[runnervm3jyl0:46713] Signal: Aborted (6)
[runnervm3jyl0:46713] Signal code:  (-6)
[runnervm3jyl0:46713] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6bef445330]
[runnervm3jyl0:46713] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6bef49eb2c]
[runnervm3jyl0:46713] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6bef44527e]
[runnervm3jyl0:46713] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6bef4288ff]
[runnervm3jyl0:46713] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6bef8a5ff5]
[runnervm3jyl0:46713] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6bef8bb0da]
[runnervm3jyl0:46713] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6bef8a5a55]
[runnervm3jyl0:46713] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6bef8a5a6f]
[runnervm3jyl0:46713] [ 8] plumed_master(+0x146dd)[0x563932c716dd]
[runnervm3jyl0:46713] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6bef42a1ca]
[runnervm3jyl0:46713] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6bef42a28b]
[runnervm3jyl0:46713] [11] plumed_master(+0x15365)[0x563932c72365]
[runnervm3jyl0:46713] *** End of error message ***
</pre>
{% endraw %}
