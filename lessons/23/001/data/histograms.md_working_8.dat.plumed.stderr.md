Stderr for source:  histograms.md_working_8.dat   
Download: [zipped raw stdout](histograms.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?

[pkrvmbietmlfzoi:36916] *** Process received signal ***
[pkrvmbietmlfzoi:36916] Signal: Aborted (6)
[pkrvmbietmlfzoi:36916] Signal code:  (-6)
[pkrvmbietmlfzoi:36915] *** Process received signal ***
[pkrvmbietmlfzoi:36915] Signal: Aborted (6)
[pkrvmbietmlfzoi:36915] Signal code:  (-6)
[pkrvmbietmlfzoi:36916] [ 0] [pkrvmbietmlfzoi:36915] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc44b445330]
[pkrvmbietmlfzoi:36916] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f39b2445330]
[pkrvmbietmlfzoi:36915] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f39b249eb2c]
[pkrvmbietmlfzoi:36915] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc44b49eb2c]
[pkrvmbietmlfzoi:36916] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f39b244527e]
[pkrvmbietmlfzoi:36915] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f39b24288ff]
[pkrvmbietmlfzoi:36915] [ 4] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc44b44527e]
[pkrvmbietmlfzoi:36916] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f39b28a5ff5]
[pkrvmbietmlfzoi:36915] [ 5] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc44b4288ff]
[pkrvmbietmlfzoi:36916] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f39b28bb0da]
[pkrvmbietmlfzoi:36915] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc44b8a5ff5]
[pkrvmbietmlfzoi:36916] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f39b28a5a55]
[pkrvmbietmlfzoi:36915] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc44b8bb0da]
[pkrvmbietmlfzoi:36916] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f39b28a5a6f]
[pkrvmbietmlfzoi:36915] [ 8] plumed(+0x13209)[0x55e08313f209]
[pkrvmbietmlfzoi:36915] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f39b242a1ca]
[pkrvmbietmlfzoi:36915] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f39b242a28b]
[pkrvmbietmlfzoi:36915] [11] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc44b8a5a55]
[pkrvmbietmlfzoi:36916] [ 7] plumed(+0x134a5)[0x55e08313f4a5]
[pkrvmbietmlfzoi:36915] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc44b8a5a6f]
[pkrvmbietmlfzoi:36916] [ 8] plumed(+0x13209)[0x56121506d209]
[pkrvmbietmlfzoi:36916] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc44b42a1ca]
[pkrvmbietmlfzoi:36916] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc44b42a28b]
[pkrvmbietmlfzoi:36916] [11] plumed(+0x134a5)[0x56121506d4a5]
[pkrvmbietmlfzoi:36916] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node pkrvmbietmlfzoi exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
