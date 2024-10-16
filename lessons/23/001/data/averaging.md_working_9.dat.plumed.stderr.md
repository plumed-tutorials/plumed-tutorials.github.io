Stderr for source:  averaging.md_working_9.dat   
Download: [zipped raw stdout](averaging.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():  terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'

(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[fv-az1426-552:06009] *** Process received signal ***
[fv-az1426-552:06009] Signal: Aborted (6)
[fv-az1426-552:06009] Signal code:  (-6)
[fv-az1426-552:06008] *** Process received signal ***
[fv-az1426-552:06008] Signal: Aborted (6)
[fv-az1426-552:06008] Signal code:  (-6)
[fv-az1426-552:06008] [ 0] [fv-az1426-552:06009] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa40ea42520]
[fv-az1426-552:06008] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa40ea969fc]
[fv-az1426-552:06008] [ 2] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa1faa42520]
[fv-az1426-552:06009] [ 1] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa40ea42476]
[fv-az1426-552:06008] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa40ea287f3]
[fv-az1426-552:06008] [ 4] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa1faa969fc]
[fv-az1426-552:06009] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa40eea2b9e]
[fv-az1426-552:06008] [ 5] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa1faa42476]
[fv-az1426-552:06009] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa1faa287f3]
[fv-az1426-552:06009] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa40eeae20c]
[fv-az1426-552:06008] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa40eeae277]
[fv-az1426-552:06008] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa1faea2b9e]
[fv-az1426-552:06009] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa40eeae52b]
[fv-az1426-552:06008] [ 8] plumed(+0x12f48)[0x55c8dd8a9f48]
[fv-az1426-552:06008] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa40ea29d90]
[fv-az1426-552:06008] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa1faeae20c]
[fv-az1426-552:06009] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa40ea29e40]
[fv-az1426-552:06008] [11] plumed(+0x131e5)[0x55c8dd8aa1e5]
[fv-az1426-552:06008] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa1faeae277]
[fv-az1426-552:06009] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa1faeae52b]
[fv-az1426-552:06009] [ 8] plumed(+0x12f48)[0x55aa2baf2f48]
[fv-az1426-552:06009] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa1faa29d90]
[fv-az1426-552:06009] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa1faa29e40]
[fv-az1426-552:06009] [11] plumed(+0x131e5)[0x55aa2baf31e5]
[fv-az1426-552:06009] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1426-552 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
