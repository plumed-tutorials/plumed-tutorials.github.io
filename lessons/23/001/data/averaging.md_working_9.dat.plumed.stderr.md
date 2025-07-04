Stderr for source:  averaging.md_working_9.dat   
Download: [zipped raw stdout](averaging.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?

[pkrvmbietmlfzoi:36610] *** Process received signal ***
[pkrvmbietmlfzoi:36610] Signal: Aborted (6)
[pkrvmbietmlfzoi:36610] Signal code:  (-6)
[pkrvmbietmlfzoi:36611] *** Process received signal ***
[pkrvmbietmlfzoi:36611] Signal: Aborted (6)
[pkrvmbietmlfzoi:36611] Signal code:  (-6)
[pkrvmbietmlfzoi:36611] [ 0] [pkrvmbietmlfzoi:36610] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f124d845330]
[pkrvmbietmlfzoi:36611] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6912645330]
[pkrvmbietmlfzoi:36610] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f124d89eb2c]
[pkrvmbietmlfzoi:36611] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f124d84527e]
[pkrvmbietmlfzoi:36611] [ 3] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f691269eb2c]
[pkrvmbietmlfzoi:36610] [ 2] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f124d8288ff]
[pkrvmbietmlfzoi:36611] [ 4] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f691264527e]
[pkrvmbietmlfzoi:36610] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f124dca5ff5]
[pkrvmbietmlfzoi:36611] [ 5] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f69126288ff]
[pkrvmbietmlfzoi:36610] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f124dcbb0da]
[pkrvmbietmlfzoi:36611] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6912aa5ff5]
[pkrvmbietmlfzoi:36610] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f124dca5a55]
[pkrvmbietmlfzoi:36611] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f124dca5a6f]
[pkrvmbietmlfzoi:36611] [ 8] plumed(+0x13209)[0x55e08939c209]
[pkrvmbietmlfzoi:36611] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6912abb0da]
[pkrvmbietmlfzoi:36610] [ 6] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f124d82a1ca]
[pkrvmbietmlfzoi:36611] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f124d82a28b]
[pkrvmbietmlfzoi:36611] [11] plumed(+0x134a5)[0x55e08939c4a5]
[pkrvmbietmlfzoi:36611] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6912aa5a55]
[pkrvmbietmlfzoi:36610] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6912aa5a6f]
[pkrvmbietmlfzoi:36610] [ 8] plumed(+0x13209)[0x55fc1d4c7209]
[pkrvmbietmlfzoi:36610] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f691262a1ca]
[pkrvmbietmlfzoi:36610] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f691262a28b]
[pkrvmbietmlfzoi:36610] [11] plumed(+0x134a5)[0x55fc1d4c74a5]
[pkrvmbietmlfzoi:36610] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node pkrvmbietmlfzoi exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
