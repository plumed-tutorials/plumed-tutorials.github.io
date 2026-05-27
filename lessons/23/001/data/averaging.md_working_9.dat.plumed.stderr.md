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
Maybe a missing space or a typo?
[runnervmg397c:80814] *** Process received signal ***
[runnervmg397c:80814] Signal: Aborted (6)
[runnervmg397c:80814] Signal code:  (-6)
[runnervmg397c:80814] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f71e8c45330]
[runnervmg397c:80814] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f71e8c9eb2c]
[runnervmg397c:80814] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f71e8c4527e]
[runnervmg397c:80814] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f71e8c288ff]
[runnervmg397c:80814] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f71e90a5ff5]
[runnervmg397c:80814] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f71e90bb0da]
[runnervmg397c:80814] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f71e90a5a55]
[runnervmg397c:80814] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f71e90a5a6f]
[runnervmg397c:80814] [ 8] plumed(+0x13209)[0x55c19043f209]
[runnervmg397c:80814] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f71e8c2a1ca]
[runnervmg397c:80814] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f71e8c2a28b]
[runnervmg397c:80814] [11] plumed(+0x134a5)[0x55c19043f4a5]
[runnervmg397c:80814] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[runnervmg397c:80815] *** Process received signal ***
[runnervmg397c:80815] Signal: Aborted (6)
[runnervmg397c:80815] Signal code:  (-6)
[runnervmg397c:80815] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f51da445330]
[runnervmg397c:80815] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f51da49eb2c]
[runnervmg397c:80815] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f51da44527e]
[runnervmg397c:80815] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f51da4288ff]
[runnervmg397c:80815] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f51da8a5ff5]
[runnervmg397c:80815] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f51da8bb0da]
[runnervmg397c:80815] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f51da8a5a55]
[runnervmg397c:80815] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f51da8a5a6f]
[runnervmg397c:80815] [ 8] plumed(+0x13209)[0x5649343eb209]
[runnervmg397c:80815] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f51da42a1ca]
[runnervmg397c:80815] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f51da42a28b]
[runnervmg397c:80815] [11] plumed(+0x134a5)[0x5649343eb4a5]
[runnervmg397c:80815] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node runnervmg397c exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
