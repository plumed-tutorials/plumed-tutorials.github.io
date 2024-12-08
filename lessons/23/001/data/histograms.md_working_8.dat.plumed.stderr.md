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
[fv-az1020-777:06137] *** Process received signal ***
[fv-az1020-777:06137] Signal: Aborted (6)
[fv-az1020-777:06137] Signal code:  (-6)
[fv-az1020-777:06137] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fef93c42520]
[fv-az1020-777:06137] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fef93c969fc]
[fv-az1020-777:06137] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fef93c42476]
[fv-az1020-777:06137] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fef93c287f3]
[fv-az1020-777:06137] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fef940a2b9e]
[fv-az1020-777:06137] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fef940ae20c]
[fv-az1020-777:06137] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fef940ae277]
[fv-az1020-777:06137] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fef940ae52b]
[fv-az1020-777:06137] [ 8] plumed(+0x12f48)[0x55cf66dfff48]
[fv-az1020-777:06137] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fef93c29d90]
[fv-az1020-777:06137] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fef93c29e40]
[fv-az1020-777:06137] [11] plumed(+0x131e5)[0x55cf66e001e5]
[fv-az1020-777:06137] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[fv-az1020-777:06138] *** Process received signal ***
[fv-az1020-777:06138] Signal: Aborted (6)
[fv-az1020-777:06138] Signal code:  (-6)
[fv-az1020-777:06138] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8379c42520]
[fv-az1020-777:06138] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8379c969fc]
[fv-az1020-777:06138] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8379c42476]
[fv-az1020-777:06138] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8379c287f3]
[fv-az1020-777:06138] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f837a0a2b9e]
[fv-az1020-777:06138] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f837a0ae20c]
[fv-az1020-777:06138] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f837a0ae277]
[fv-az1020-777:06138] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f837a0ae52b]
[fv-az1020-777:06138] [ 8] plumed(+0x12f48)[0x55d1ac03bf48]
[fv-az1020-777:06138] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8379c29d90]
[fv-az1020-777:06138] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8379c29e40]
[fv-az1020-777:06138] [11] plumed(+0x131e5)[0x55d1ac03c1e5]
[fv-az1020-777:06138] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1020-777 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
