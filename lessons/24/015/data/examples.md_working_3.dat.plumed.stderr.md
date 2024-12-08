Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1079) void PLMD::PlumedMain::load(const string&)
I cannot load library path/to/PythonCVInterface.so path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1778-96:04500] *** Process received signal ***
[fv-az1778-96:04500] Signal: Aborted (6)
[fv-az1778-96:04500] Signal code:  (-6)
[fv-az1778-96:04500] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f33b5242520]
[fv-az1778-96:04500] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f33b52969fc]
[fv-az1778-96:04500] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f33b5242476]
[fv-az1778-96:04500] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f33b52287f3]
[fv-az1778-96:04500] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f33b56a2b9e]
[fv-az1778-96:04500] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f33b56ae20c]
[fv-az1778-96:04500] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f33b56ae277]
[fv-az1778-96:04500] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f33b56ae52b]
[fv-az1778-96:04500] [ 8] plumed(+0x12f48)[0x56430865cf48]
[fv-az1778-96:04500] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f33b5229d90]
[fv-az1778-96:04500] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f33b5229e40]
[fv-az1778-96:04500] [11] plumed(+0x131e5)[0x56430865d1e5]
[fv-az1778-96:04500] *** End of error message ***
</pre>
{% endraw %}
