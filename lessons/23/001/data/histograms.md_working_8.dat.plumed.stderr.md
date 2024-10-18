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
[fv-az1535-978:71384] *** Process received signal ***
[fv-az1535-978:71384] Signal: Aborted (6)
[fv-az1535-978:71384] Signal code:  (-6)
[fv-az1535-978:71384] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4e80a42520]
[fv-az1535-978:71384] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4e80a969fc]
[fv-az1535-978:71384] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4e80a42476]
[fv-az1535-978:71384] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4e80a287f3]
[fv-az1535-978:71384] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4e80ea2b9e]
[fv-az1535-978:71384] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4e80eae20c]
[fv-az1535-978:71384] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4e80eae277]
[fv-az1535-978:71384] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4e80eae52b]
[fv-az1535-978:71384] [ 8] plumed(+0x12f48)[0x55b28dab0f48]
[fv-az1535-978:71384] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4e80a29d90]
[fv-az1535-978:71384] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4e80a29e40]
[fv-az1535-978:71384] [11] plumed(+0x131e5)[0x55b28dab11e5]
[fv-az1535-978:71384] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[fv-az1535-978:71383] *** Process received signal ***
[fv-az1535-978:71383] Signal: Aborted (6)
[fv-az1535-978:71383] Signal code:  (-6)
[fv-az1535-978:71383] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f9b2f042520]
[fv-az1535-978:71383] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f9b2f0969fc]
[fv-az1535-978:71383] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f9b2f042476]
[fv-az1535-978:71383] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f9b2f0287f3]
[fv-az1535-978:71383] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f9b2f4a2b9e]
[fv-az1535-978:71383] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f9b2f4ae20c]
[fv-az1535-978:71383] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f9b2f4ae277]
[fv-az1535-978:71383] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f9b2f4ae52b]
[fv-az1535-978:71383] [ 8] plumed(+0x12f48)[0x5607305c1f48]
[fv-az1535-978:71383] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f9b2f029d90]
[fv-az1535-978:71383] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f9b2f029e40]
[fv-az1535-978:71383] [11] plumed(+0x131e5)[0x5607305c21e5]
[fv-az1535-978:71383] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1535-978 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
