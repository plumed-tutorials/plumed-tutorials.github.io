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
[fv-az1690-151:05505] *** Process received signal ***
[fv-az1690-151:05505] Signal: Aborted (6)
[fv-az1690-151:05505] Signal code:  (-6)
[fv-az1690-151:05505] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc05e645330]
[fv-az1690-151:05505] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc05e69eb2c]
[fv-az1690-151:05505] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc05e64527e]
[fv-az1690-151:05505] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc05e6288ff]
[fv-az1690-151:05505] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc05eaa5ff5]
[fv-az1690-151:05505] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc05eabb0da]
[fv-az1690-151:05505] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc05eaa5a55]
[fv-az1690-151:05505] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc05eaa5a6f]
[fv-az1690-151:05505] [ 8] plumed_master(+0x146dd)[0x55e2982bf6dd]
[fv-az1690-151:05505] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc05e62a1ca]
[fv-az1690-151:05505] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc05e62a28b]
[fv-az1690-151:05505] [11] plumed_master(+0x15365)[0x55e2982c0365]
[fv-az1690-151:05505] *** End of error message ***
</pre>
{% endraw %}
