Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/DLLoader.cpp:50) void* PLMD::DLLoader::load(const std::string&)
Could not load library path/to/PythonCVInterface.so
path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1279-640:05530] *** Process received signal ***
[fv-az1279-640:05530] Signal: Aborted (6)
[fv-az1279-640:05530] Signal code:  (-6)
[fv-az1279-640:05530] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb963a45330]
[fv-az1279-640:05530] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb963a9eb2c]
[fv-az1279-640:05530] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb963a4527e]
[fv-az1279-640:05530] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb963a288ff]
[fv-az1279-640:05530] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb963ea5ff5]
[fv-az1279-640:05530] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb963ebb0da]
[fv-az1279-640:05530] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb963ea5a55]
[fv-az1279-640:05530] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb963ea5a6f]
[fv-az1279-640:05530] [ 8] plumed_master(+0x146dd)[0x55ce8436d6dd]
[fv-az1279-640:05530] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb963a2a1ca]
[fv-az1279-640:05530] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb963a2a28b]
[fv-az1279-640:05530] [11] plumed_master(+0x15365)[0x55ce8436e365]
[fv-az1279-640:05530] *** End of error message ***
</pre>
{% endraw %}
