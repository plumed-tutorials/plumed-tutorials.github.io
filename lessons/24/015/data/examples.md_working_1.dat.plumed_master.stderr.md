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
[pkrvmbietmlfzoi:35259] *** Process received signal ***
[pkrvmbietmlfzoi:35259] Signal: Aborted (6)
[pkrvmbietmlfzoi:35259] Signal code:  (-6)
[pkrvmbietmlfzoi:35259] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5051445330]
[pkrvmbietmlfzoi:35259] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f505149eb2c]
[pkrvmbietmlfzoi:35259] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f505144527e]
[pkrvmbietmlfzoi:35259] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f50514288ff]
[pkrvmbietmlfzoi:35259] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f50518a5ff5]
[pkrvmbietmlfzoi:35259] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f50518bb0da]
[pkrvmbietmlfzoi:35259] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f50518a5a55]
[pkrvmbietmlfzoi:35259] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f50518a5a6f]
[pkrvmbietmlfzoi:35259] [ 8] plumed_master(+0x146dd)[0x55dcb46a36dd]
[pkrvmbietmlfzoi:35259] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f505142a1ca]
[pkrvmbietmlfzoi:35259] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f505142a28b]
[pkrvmbietmlfzoi:35259] [11] plumed_master(+0x15365)[0x55dcb46a4365]
[pkrvmbietmlfzoi:35259] *** End of error message ***
</pre>
{% endraw %}
