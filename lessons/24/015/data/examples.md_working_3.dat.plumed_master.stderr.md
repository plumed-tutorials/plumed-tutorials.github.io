Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(tools/DLLoader.cpp:49) void* PLMD::DLLoader::load(const string&)
Could not load library path/to/PythonCVInterface.so
path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1778-96:04508] *** Process received signal ***
[fv-az1778-96:04508] Signal: Aborted (6)
[fv-az1778-96:04508] Signal code:  (-6)
[fv-az1778-96:04508] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa94b042520]
[fv-az1778-96:04508] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa94b0969fc]
[fv-az1778-96:04508] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa94b042476]
[fv-az1778-96:04508] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa94b0287f3]
[fv-az1778-96:04508] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa94b4a2b9e]
[fv-az1778-96:04508] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa94b4ae20c]
[fv-az1778-96:04508] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa94b4ae277]
[fv-az1778-96:04508] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa94b4ae52b]
[fv-az1778-96:04508] [ 8] plumed_master(+0x14254)[0x55f69d450254]
[fv-az1778-96:04508] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa94b029d90]
[fv-az1778-96:04508] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa94b029e40]
[fv-az1778-96:04508] [11] plumed_master(+0x14eb5)[0x55f69d450eb5]
[fv-az1778-96:04508] *** End of error message ***
</pre>
{% endraw %}
