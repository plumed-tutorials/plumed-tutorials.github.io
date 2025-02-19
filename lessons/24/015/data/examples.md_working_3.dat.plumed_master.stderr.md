Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/DLLoader.cpp:50) void* PLMD::DLLoader::load(const std::string&)
Could not load library path/to/PythonCVInterface.so
path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1690-151:05591] *** Process received signal ***
[fv-az1690-151:05591] Signal: Aborted (6)
[fv-az1690-151:05591] Signal code:  (-6)
[fv-az1690-151:05591] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2fa2845330]
[fv-az1690-151:05591] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2fa289eb2c]
[fv-az1690-151:05591] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2fa284527e]
[fv-az1690-151:05591] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2fa28288ff]
[fv-az1690-151:05591] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2fa2ca5ff5]
[fv-az1690-151:05591] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2fa2cbb0da]
[fv-az1690-151:05591] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2fa2ca5a55]
[fv-az1690-151:05591] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2fa2ca5a6f]
[fv-az1690-151:05591] [ 8] plumed_master(+0x146dd)[0x5654e64a06dd]
[fv-az1690-151:05591] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2fa282a1ca]
[fv-az1690-151:05591] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2fa282a28b]
[fv-az1690-151:05591] [11] plumed_master(+0x15365)[0x5654e64a1365]
[fv-az1690-151:05591] *** End of error message ***
</pre>
{% endraw %}
