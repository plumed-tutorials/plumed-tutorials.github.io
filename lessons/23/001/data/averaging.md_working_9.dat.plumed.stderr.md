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
[runnervm3jyl0:48781] *** Process received signal ***
[runnervm3jyl0:48781] Signal: Aborted (6)
[runnervm3jyl0:48781] Signal code:  (-6)
[runnervm3jyl0:48781] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4ac4245330]
[runnervm3jyl0:48781] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4ac429eb2c]
[runnervm3jyl0:48781] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4ac424527e]
[runnervm3jyl0:48781] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4ac42288ff]
[runnervm3jyl0:48781] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4ac46a5ff5]
[runnervm3jyl0:48781] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4ac46bb0da]
[runnervm3jyl0:48781] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4ac46a5a55]
[runnervm3jyl0:48781] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4ac46a5a6f]
[runnervm3jyl0:48781] [ 8] plumed(+0x13209)[0x558871f5e209]
[runnervm3jyl0:48781] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4ac422a1ca]
[runnervm3jyl0:48781] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4ac422a28b]
[runnervm3jyl0:48781] [11] plumed(+0x134a5)[0x558871f5e4a5]
[runnervm3jyl0:48781] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[runnervm3jyl0:48780] *** Process received signal ***
[runnervm3jyl0:48780] Signal: Aborted (6)
[runnervm3jyl0:48780] Signal code:  (-6)
[runnervm3jyl0:48780] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc43da45330]
[runnervm3jyl0:48780] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc43da9eb2c]
[runnervm3jyl0:48780] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc43da4527e]
[runnervm3jyl0:48780] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc43da288ff]
[runnervm3jyl0:48780] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc43dea5ff5]
[runnervm3jyl0:48780] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc43debb0da]
[runnervm3jyl0:48780] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc43dea5a55]
[runnervm3jyl0:48780] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc43dea5a6f]
[runnervm3jyl0:48780] [ 8] plumed(+0x13209)[0x55f994791209]
[runnervm3jyl0:48780] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc43da2a1ca]
[runnervm3jyl0:48780] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc43da2a28b]
[runnervm3jyl0:48780] [11] plumed(+0x134a5)[0x55f9947914a5]
[runnervm3jyl0:48780] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node runnervm3jyl0 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
