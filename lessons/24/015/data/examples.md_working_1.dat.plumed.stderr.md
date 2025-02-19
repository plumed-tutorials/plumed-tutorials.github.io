Stderr for source:  examples.md_working_1.dat   
Download: [zipped raw stdout](examples.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:1227) void PLMD::PlumedMain::load(const std::string&)
I cannot load library /path/to/PythonCVInterface.so /path/to/PythonCVInterface.so: cannot open shared object file: No such file or directory
[fv-az1690-151:05489] *** Process received signal ***
[fv-az1690-151:05489] Signal: Aborted (6)
[fv-az1690-151:05489] Signal code:  (-6)
[fv-az1690-151:05489] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa767e45330]
[fv-az1690-151:05489] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa767e9eb2c]
[fv-az1690-151:05489] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa767e4527e]
[fv-az1690-151:05489] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa767e288ff]
[fv-az1690-151:05489] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa7682a5ff5]
[fv-az1690-151:05489] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa7682bb0da]
[fv-az1690-151:05489] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa7682a5a55]
[fv-az1690-151:05489] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa7682a5a6f]
[fv-az1690-151:05489] [ 8] plumed(+0x13209)[0x5632db00e209]
[fv-az1690-151:05489] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa767e2a1ca]
[fv-az1690-151:05489] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa767e2a28b]
[fv-az1690-151:05489] [11] plumed(+0x134a5)[0x5632db00e4a5]
[fv-az1690-151:05489] *** End of error message ***
</pre>
{% endraw %}
