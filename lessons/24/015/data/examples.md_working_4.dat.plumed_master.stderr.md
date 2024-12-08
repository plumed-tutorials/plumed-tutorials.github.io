Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/DLLoader.cpp:49) void* PLMD::DLLoader::load(const string&)
Could not load library path/to/PythonCVInterface.so
path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1778-96:04540] *** Process received signal ***
[fv-az1778-96:04540] Signal: Aborted (6)
[fv-az1778-96:04540] Signal code:  (-6)
[fv-az1778-96:04540] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe0fa042520]
[fv-az1778-96:04540] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe0fa0969fc]
[fv-az1778-96:04540] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe0fa042476]
[fv-az1778-96:04540] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe0fa0287f3]
[fv-az1778-96:04540] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe0fa4a2b9e]
[fv-az1778-96:04540] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe0fa4ae20c]
[fv-az1778-96:04540] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe0fa4ae277]
[fv-az1778-96:04540] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe0fa4ae52b]
[fv-az1778-96:04540] [ 8] plumed_master(+0x14254)[0x5592ff520254]
[fv-az1778-96:04540] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe0fa029d90]
[fv-az1778-96:04540] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe0fa029e40]
[fv-az1778-96:04540] [11] plumed_master(+0x14eb5)[0x5592ff520eb5]
[fv-az1778-96:04540] *** End of error message ***
</pre>
{% endraw %}
