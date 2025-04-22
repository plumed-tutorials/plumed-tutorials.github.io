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
[fv-az1279-640:05575] *** Process received signal ***
[fv-az1279-640:05575] Signal: Aborted (6)
[fv-az1279-640:05575] Signal code:  (-6)
[fv-az1279-640:05575] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3a26045330]
[fv-az1279-640:05575] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3a2609eb2c]
[fv-az1279-640:05575] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3a2604527e]
[fv-az1279-640:05575] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3a260288ff]
[fv-az1279-640:05575] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3a264a5ff5]
[fv-az1279-640:05575] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3a264bb0da]
[fv-az1279-640:05575] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3a264a5a55]
[fv-az1279-640:05575] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3a264a5a6f]
[fv-az1279-640:05575] [ 8] plumed_master(+0x146dd)[0x5596a4cb76dd]
[fv-az1279-640:05575] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3a2602a1ca]
[fv-az1279-640:05575] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3a2602a28b]
[fv-az1279-640:05575] [11] plumed_master(+0x15365)[0x5596a4cb8365]
[fv-az1279-640:05575] *** End of error message ***
</pre>
{% endraw %}
