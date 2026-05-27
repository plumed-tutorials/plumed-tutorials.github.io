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
[runnervm3jyl0:79506] *** Process received signal ***
[runnervm3jyl0:79506] Signal: Aborted (6)
[runnervm3jyl0:79506] Signal code:  (-6)
[runnervm3jyl0:79506] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f70b1c45330]
[runnervm3jyl0:79506] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f70b1c9eb2c]
[runnervm3jyl0:79506] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f70b1c4527e]
[runnervm3jyl0:79506] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f70b1c288ff]
[runnervm3jyl0:79506] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f70b20a5ff5]
[runnervm3jyl0:79506] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f70b20bb0da]
[runnervm3jyl0:79506] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f70b20a5a55]
[runnervm3jyl0:79506] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f70b20a5a6f]
[runnervm3jyl0:79506] [ 8] plumed_master(+0x146dd)[0x5643f3ab76dd]
[runnervm3jyl0:79506] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f70b1c2a1ca]
[runnervm3jyl0:79506] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f70b1c2a28b]
[runnervm3jyl0:79506] [11] plumed_master(+0x15365)[0x5643f3ab8365]
[runnervm3jyl0:79506] *** End of error message ***
</pre>
{% endraw %}
