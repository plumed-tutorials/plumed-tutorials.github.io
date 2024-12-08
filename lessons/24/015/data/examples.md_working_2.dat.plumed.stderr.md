Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1079) void PLMD::PlumedMain::load(const string&)
I cannot load library path/to/PythonCVInterface.so path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1778-96:04477] *** Process received signal ***
[fv-az1778-96:04477] Signal: Aborted (6)
[fv-az1778-96:04477] Signal code:  (-6)
[fv-az1778-96:04477] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd39f042520]
[fv-az1778-96:04477] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd39f0969fc]
[fv-az1778-96:04477] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd39f042476]
[fv-az1778-96:04477] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd39f0287f3]
[fv-az1778-96:04477] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd39f4a2b9e]
[fv-az1778-96:04477] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd39f4ae20c]
[fv-az1778-96:04477] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd39f4ae277]
[fv-az1778-96:04477] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd39f4ae52b]
[fv-az1778-96:04477] [ 8] plumed(+0x12f48)[0x555bd3aa4f48]
[fv-az1778-96:04477] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd39f029d90]
[fv-az1778-96:04477] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd39f029e40]
[fv-az1778-96:04477] [11] plumed(+0x131e5)[0x555bd3aa51e5]
[fv-az1778-96:04477] *** End of error message ***
</pre>
{% endraw %}
