Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1227) void PLMD::PlumedMain::load(const std::string&)
I cannot load library path/to/PythonCVInterface.so path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1690-151:05577] *** Process received signal ***
[fv-az1690-151:05577] Signal: Aborted (6)
[fv-az1690-151:05577] Signal code:  (-6)
[fv-az1690-151:05577] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f54a2a45330]
[fv-az1690-151:05577] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f54a2a9eb2c]
[fv-az1690-151:05577] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f54a2a4527e]
[fv-az1690-151:05577] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f54a2a288ff]
[fv-az1690-151:05577] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f54a2ea5ff5]
[fv-az1690-151:05577] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f54a2ebb0da]
[fv-az1690-151:05577] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f54a2ea5a55]
[fv-az1690-151:05577] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f54a2ea5a6f]
[fv-az1690-151:05577] [ 8] plumed(+0x13209)[0x55a6890b9209]
[fv-az1690-151:05577] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f54a2a2a1ca]
[fv-az1690-151:05577] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f54a2a2a28b]
[fv-az1690-151:05577] [11] plumed(+0x134a5)[0x55a6890b94a5]
[fv-az1690-151:05577] *** End of error message ***
</pre>
{% endraw %}
