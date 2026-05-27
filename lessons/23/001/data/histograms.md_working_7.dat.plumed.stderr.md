Stderr for source:  histograms.md_working_7.dat   
Download: [zipped raw stdout](histograms.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_7.dat.plumed.stderr.txt.zip) 
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
[runnervmg397c:81088] *** Process received signal ***
[runnervmg397c:81088] Signal: Aborted (6)
[runnervmg397c:81088] Signal code:  (-6)
[runnervmg397c:81088] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4f4ac45330]
[runnervmg397c:81088] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4f4ac9eb2c]
[runnervmg397c:81088] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4f4ac4527e]
[runnervmg397c:81088] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4f4ac288ff]
[runnervmg397c:81088] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4f4b0a5ff5]
[runnervmg397c:81088] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4f4b0bb0da]
[runnervmg397c:81088] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4f4b0a5a55]
[runnervmg397c:81088] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4f4b0a5a6f]
[runnervmg397c:81088] [ 8] plumed(+0x13209)[0x55b227188209]
[runnervmg397c:81088] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4f4ac2a1ca]
[runnervmg397c:81088] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4f4ac2a28b]
[runnervmg397c:81088] [11] plumed(+0x134a5)[0x55b2271884a5]
[runnervmg397c:81088] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[runnervmg397c:81089] *** Process received signal ***
[runnervmg397c:81089] Signal: Aborted (6)
[runnervmg397c:81089] Signal code:  (-6)
[runnervmg397c:81089] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f76c6a45330]
[runnervmg397c:81089] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f76c6a9eb2c]
[runnervmg397c:81089] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f76c6a4527e]
[runnervmg397c:81089] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f76c6a288ff]
[runnervmg397c:81089] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f76c6ea5ff5]
[runnervmg397c:81089] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f76c6ebb0da]
[runnervmg397c:81089] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f76c6ea5a55]
[runnervmg397c:81089] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f76c6ea5a6f]
[runnervmg397c:81089] [ 8] plumed(+0x13209)[0x559efd893209]
[runnervmg397c:81089] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f76c6a2a1ca]
[runnervmg397c:81089] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f76c6a2a28b]
[runnervmg397c:81089] [11] plumed(+0x134a5)[0x559efd8934a5]
[runnervmg397c:81089] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node runnervmg397c exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
