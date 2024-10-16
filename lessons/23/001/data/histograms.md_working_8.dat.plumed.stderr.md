Stderr for source:  histograms.md_working_8.dat   
Download: [zipped raw stdout](histograms.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[fv-az1426-552:06225] *** Process received signal ***
[fv-az1426-552:06225] Signal: Aborted (6)
[fv-az1426-552:06225] Signal code:  (-6)
[fv-az1426-552:06225] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2953e42520]
[fv-az1426-552:06225] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f2953e969fc]
[fv-az1426-552:06225] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2953e42476]
[fv-az1426-552:06225] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f2953e287f3]
[fv-az1426-552:06225] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f29542a2b9e]
[fv-az1426-552:06225] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f29542ae20c]
[fv-az1426-552:06225] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f29542ae277]
[fv-az1426-552:06225] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f29542ae52b]
[fv-az1426-552:06225] [ 8] plumed(+0x12f48)[0x562e0db8bf48]
[fv-az1426-552:06225] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2953e29d90]
[fv-az1426-552:06225] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2953e29e40]
[fv-az1426-552:06225] [11] plumed(+0x131e5)[0x562e0db8c1e5]
[fv-az1426-552:06225] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[fv-az1426-552:06226] *** Process received signal ***
[fv-az1426-552:06226] Signal: Aborted (6)
[fv-az1426-552:06226] Signal code:  (-6)
[fv-az1426-552:06226] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1e25242520]
[fv-az1426-552:06226] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1e252969fc]
[fv-az1426-552:06226] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1e25242476]
[fv-az1426-552:06226] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1e252287f3]
[fv-az1426-552:06226] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1e256a2b9e]
[fv-az1426-552:06226] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1e256ae20c]
[fv-az1426-552:06226] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1e256ae277]
[fv-az1426-552:06226] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1e256ae52b]
[fv-az1426-552:06226] [ 8] plumed(+0x12f48)[0x56099fe02f48]
[fv-az1426-552:06226] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1e25229d90]
[fv-az1426-552:06226] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1e25229e40]
[fv-az1426-552:06226] [11] plumed(+0x131e5)[0x56099fe031e5]
[fv-az1426-552:06226] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node fv-az1426-552 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
