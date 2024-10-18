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
[fv-az1535-978:71169] *** Process received signal ***
[fv-az1535-978:71169] Signal: Aborted (6)
[fv-az1535-978:71169] Signal code:  (-6)
[fv-az1535-978:71169] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fdcdc442520]
[fv-az1535-978:71169] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fdcdc4969fc]
[fv-az1535-978:71169] [ 2] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
/lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fdcdc442476]
[fv-az1535-978:71169] [ 3] [fv-az1535-978:71170] *** Process received signal ***
[fv-az1535-978:71170] Signal: Aborted (6)
[fv-az1535-978:71170] Signal code:  (-6)
/lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fdcdc4287f3]
[fv-az1535-978:71169] [ 4] [fv-az1535-978:71170] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa6b6842520]
[fv-az1535-978:71170] [ 1] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fdcdc8a2b9e]
[fv-az1535-978:71169] [ 5] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa6b68969fc]
[fv-az1535-978:71170] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fdcdc8ae20c]
[fv-az1535-978:71169] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fdcdc8ae277]
[fv-az1535-978:71169] [ 7] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa6b6842476]
[fv-az1535-978:71170] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fdcdc8ae52b]
[fv-az1535-978:71169] [ 8] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa6b68287f3]
[fv-az1535-978:71170] [ 4] plumed(+0x12f48)[0x55deaa935f48]
[fv-az1535-978:71169] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fdcdc429d90]
[fv-az1535-978:71169] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fdcdc429e40]
[fv-az1535-978:71169] [11] plumed(+0x131e5)[0x55deaa9361e5]
[fv-az1535-978:71169] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa6b6ca2b9e]
[fv-az1535-978:71170] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa6b6cae20c]
[fv-az1535-978:71170] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa6b6cae277]
[fv-az1535-978:71170] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa6b6cae52b]
[fv-az1535-978:71170] [ 8] plumed(+0x12f48)[0x55c96500ff48]
[fv-az1535-978:71170] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa6b6829d90]
[fv-az1535-978:71170] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa6b6829e40]
[fv-az1535-978:71170] [11] plumed(+0x131e5)[0x55c9650101e5]
[fv-az1535-978:71170] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1535-978 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
