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
[runnervm3jyl0:46697] *** Process received signal ***
[runnervm3jyl0:46697] Signal: Aborted (6)
[runnervm3jyl0:46697] Signal code:  (-6)
[runnervm3jyl0:46697] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe4dee45330]
[runnervm3jyl0:46697] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe4dee9eb2c]
[runnervm3jyl0:46697] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe4dee4527e]
[runnervm3jyl0:46697] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe4dee288ff]
[runnervm3jyl0:46697] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe4df2a5ff5]
[runnervm3jyl0:46697] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe4df2bb0da]
[runnervm3jyl0:46697] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe4df2a5a55]
[runnervm3jyl0:46697] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe4df2a5a6f]
[runnervm3jyl0:46697] [ 8] plumed(+0x13209)[0x559416c08209]
[runnervm3jyl0:46697] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe4dee2a1ca]
[runnervm3jyl0:46697] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe4dee2a28b]
[runnervm3jyl0:46697] [11] plumed(+0x134a5)[0x559416c084a5]
[runnervm3jyl0:46697] *** End of error message ***
</pre>
{% endraw %}
