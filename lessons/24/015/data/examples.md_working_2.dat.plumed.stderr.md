Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1227) void PLMD::PlumedMain::load(const std::string&)
I cannot load library path/to/PythonCVInterface.so path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1279-640:05514] *** Process received signal ***
[fv-az1279-640:05514] Signal: Aborted (6)
[fv-az1279-640:05514] Signal code:  (-6)
[fv-az1279-640:05514] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f084ce45330]
[fv-az1279-640:05514] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f084ce9eb2c]
[fv-az1279-640:05514] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f084ce4527e]
[fv-az1279-640:05514] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f084ce288ff]
[fv-az1279-640:05514] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f084d2a5ff5]
[fv-az1279-640:05514] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f084d2bb0da]
[fv-az1279-640:05514] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f084d2a5a55]
[fv-az1279-640:05514] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f084d2a5a6f]
[fv-az1279-640:05514] [ 8] plumed(+0x13209)[0x55591717b209]
[fv-az1279-640:05514] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f084ce2a1ca]
[fv-az1279-640:05514] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f084ce2a28b]
[fv-az1279-640:05514] [11] plumed(+0x134a5)[0x55591717b4a5]
[fv-az1279-640:05514] *** End of error message ***
</pre>
{% endraw %}
