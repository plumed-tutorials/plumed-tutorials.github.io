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
Maybe a missing space or a typo?
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
[fv-az1755-505:07930] *** Process received signal ***
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[fv-az1755-505:07930] Signal: Aborted (6)
[fv-az1755-505:07930] Signal code:  (-6)
[fv-az1755-505:07929] *** Process received signal ***
[fv-az1755-505:07929] Signal: Aborted (6)
[fv-az1755-505:07929] Signal code:  (-6)
[fv-az1755-505:07930] [ 0] [fv-az1755-505:07929] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe871845330]
[fv-az1755-505:07930] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4c4f645330]
[fv-az1755-505:07929] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4c4f69eb2c]
[fv-az1755-505:07929] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe87189eb2c]
[fv-az1755-505:07930] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4c4f64527e]
[fv-az1755-505:07929] [ 3] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe87184527e]
[fv-az1755-505:07930] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4c4f6288ff]
[fv-az1755-505:07929] [ 4] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe8718288ff]
[fv-az1755-505:07930] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4c4faa5ff5]
[fv-az1755-505:07929] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe871ca5ff5]
[fv-az1755-505:07930] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4c4fabb0da]
[fv-az1755-505:07929] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4c4faa5a55]
[fv-az1755-505:07929] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe871cbb0da]
[fv-az1755-505:07930] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4c4faa5a6f]
[fv-az1755-505:07929] [ 8] plumed(+0x13209)[0x55c051bb9209]
[fv-az1755-505:07929] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4c4f62a1ca]
[fv-az1755-505:07929] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe871ca5a55]
[fv-az1755-505:07930] [ 7] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4c4f62a28b]
[fv-az1755-505:07929] [11] plumed(+0x134a5)[0x55c051bb94a5]
[fv-az1755-505:07929] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe871ca5a6f]
[fv-az1755-505:07930] [ 8] plumed(+0x13209)[0x564b1f301209]
[fv-az1755-505:07930] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe87182a1ca]
[fv-az1755-505:07930] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe87182a28b]
[fv-az1755-505:07930] [11] plumed(+0x134a5)[0x564b1f3014a5]
[fv-az1755-505:07930] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node fv-az1755-505 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
