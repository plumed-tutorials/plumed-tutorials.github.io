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
[fv-az1690-151:05549] *** Process received signal ***
[fv-az1690-151:05549] Signal: Aborted (6)
[fv-az1690-151:05549] Signal code:  (-6)
[fv-az1690-151:05549] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd327445330]
[fv-az1690-151:05549] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd32749eb2c]
[fv-az1690-151:05549] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd32744527e]
[fv-az1690-151:05549] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd3274288ff]
[fv-az1690-151:05549] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd3278a5ff5]
[fv-az1690-151:05549] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd3278bb0da]
[fv-az1690-151:05549] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd3278a5a55]
[fv-az1690-151:05549] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd3278a5a6f]
[fv-az1690-151:05549] [ 8] plumed_master(+0x146dd)[0x55b93c4586dd]
[fv-az1690-151:05549] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd32742a1ca]
[fv-az1690-151:05549] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd32742a28b]
[fv-az1690-151:05549] [11] plumed_master(+0x15365)[0x55b93c459365]
[fv-az1690-151:05549] *** End of error message ***
</pre>
{% endraw %}
