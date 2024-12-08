Stderr for source:  averaging.md_working_9.dat   
Download: [zipped raw stdout](averaging.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[fv-az1020-777:05922] *** Process received signal ***
[fv-az1020-777:05922] Signal: Aborted (6)
[fv-az1020-777:05922] Signal code:  (-6)
[fv-az1020-777:05922] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb683a42520]
[fv-az1020-777:05922] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb683a969fc]
[fv-az1020-777:05922] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb683a42476]
[fv-az1020-777:05922] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb683a287f3]
[fv-az1020-777:05922] [ 4] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb683ea2b9e]
[fv-az1020-777:05922] [ 5] [fv-az1020-777:05923] *** Process received signal ***
[fv-az1020-777:05923] Signal: Aborted (6)
[fv-az1020-777:05923] Signal code:  (-6)
[fv-az1020-777:05923] [ 0] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb683eae20c]
[fv-az1020-777:05922] [ 6] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f5ac2a42520]
[fv-az1020-777:05923] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f5ac2a969fc]
[fv-az1020-777:05923] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb683eae277]
[fv-az1020-777:05922] [ 7] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f5ac2a42476]
[fv-az1020-777:05923] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb683eae52b]
[fv-az1020-777:05922] [ 8] plumed(+0x12f48)[0x55ecad9cff48]
[fv-az1020-777:05922] [ 9] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f5ac2a287f3]
[fv-az1020-777:05923] [ 4] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb683a29d90]
[fv-az1020-777:05922] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f5ac2ea2b9e]
[fv-az1020-777:05923] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f5ac2eae20c]
[fv-az1020-777:05923] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb683a29e40]
[fv-az1020-777:05922] [11] plumed(+0x131e5)[0x55ecad9d01e5]
[fv-az1020-777:05922] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f5ac2eae277]
[fv-az1020-777:05923] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f5ac2eae52b]
[fv-az1020-777:05923] [ 8] plumed(+0x12f48)[0x5619941bcf48]
[fv-az1020-777:05923] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f5ac2a29d90]
[fv-az1020-777:05923] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f5ac2a29e40]
[fv-az1020-777:05923] [11] plumed(+0x131e5)[0x5619941bd1e5]
[fv-az1020-777:05923] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1020-777 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
