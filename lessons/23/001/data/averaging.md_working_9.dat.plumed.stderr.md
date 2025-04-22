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
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[fv-az1315-757:07722] *** Process received signal ***
[fv-az1315-757:07722] Signal: Aborted (6)
[fv-az1315-757:07722] Signal code:  (-6)
[fv-az1315-757:07723] *** Process received signal ***
[fv-az1315-757:07723] Signal: Aborted (6)
[fv-az1315-757:07723] Signal code:  (-6)
[fv-az1315-757:07722] [ 0] [fv-az1315-757:07723] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff616a45330]
[fv-az1315-757:07722] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff616a9eb2c]
[fv-az1315-757:07722] [ 2] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0aa4445330]
[fv-az1315-757:07723] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0aa449eb2c]
[fv-az1315-757:07723] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff616a4527e]
[fv-az1315-757:07722] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff616a288ff]
[fv-az1315-757:07722] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff616ea5ff5]
[fv-az1315-757:07722] [ 5] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0aa444527e]
[fv-az1315-757:07723] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0aa44288ff]
[fv-az1315-757:07723] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff616ebb0da]
[fv-az1315-757:07722] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff616ea5a55]
[fv-az1315-757:07722] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0aa48a5ff5]
[fv-az1315-757:07723] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff616ea5a6f]
[fv-az1315-757:07722] [ 8] plumed(+0x13209)[0x55a3f842c209]
[fv-az1315-757:07722] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff616a2a1ca]
[fv-az1315-757:07722] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0aa48bb0da]
[fv-az1315-757:07723] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff616a2a28b]
[fv-az1315-757:07722] [11] plumed(+0x134a5)[0x55a3f842c4a5]
[fv-az1315-757:07722] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0aa48a5a55]
[fv-az1315-757:07723] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0aa48a5a6f]
[fv-az1315-757:07723] [ 8] plumed(+0x13209)[0x557b7f1f2209]
[fv-az1315-757:07723] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0aa442a1ca]
[fv-az1315-757:07723] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0aa442a28b]
[fv-az1315-757:07723] [11] plumed(+0x134a5)[0x557b7f1f24a5]
[fv-az1315-757:07723] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1315-757 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
