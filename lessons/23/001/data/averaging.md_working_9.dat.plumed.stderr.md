Stderr for source:  averaging.md_working_9.dat   
Download: [zipped raw stdout](averaging.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[fv-az1755-505:07624] *** Process received signal ***
[fv-az1755-505:07625] *** Process received signal ***
[fv-az1755-505:07625] Signal: Aborted (6)
[fv-az1755-505:07625] Signal code:  (-6)
[fv-az1755-505:07624] Signal: Aborted (6)
[fv-az1755-505:07624] Signal code:  (-6)
[fv-az1755-505:07624] [ 0] [fv-az1755-505:07625] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1ca7e45330]
[fv-az1755-505:07625] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fab16445330]
[fv-az1755-505:07624] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fab1649eb2c]
[fv-az1755-505:07624] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1ca7e9eb2c]
[fv-az1755-505:07625] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fab1644527e]
[fv-az1755-505:07624] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fab164288ff]
[fv-az1755-505:07624] [ 4] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1ca7e4527e]
[fv-az1755-505:07625] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fab168a5ff5]
[fv-az1755-505:07624] [ 5] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1ca7e288ff]
[fv-az1755-505:07625] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fab168bb0da]
[fv-az1755-505:07624] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1ca82a5ff5]
[fv-az1755-505:07625] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fab168a5a55]
[fv-az1755-505:07624] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fab168a5a6f]
[fv-az1755-505:07624] [ 8] plumed(+0x13209)[0x556da915a209]
[fv-az1755-505:07624] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1ca82bb0da]
[fv-az1755-505:07625] [ 6] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fab1642a1ca]
[fv-az1755-505:07624] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fab1642a28b]
[fv-az1755-505:07624] [11] plumed(+0x134a5)[0x556da915a4a5]
[fv-az1755-505:07624] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1ca82a5a55]
[fv-az1755-505:07625] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1ca82a5a6f]
[fv-az1755-505:07625] [ 8] plumed(+0x13209)[0x5628ec5e3209]
[fv-az1755-505:07625] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1ca7e2a1ca]
[fv-az1755-505:07625] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1ca7e2a28b]
[fv-az1755-505:07625] [11] plumed(+0x134a5)[0x5628ec5e34a5]
[fv-az1755-505:07625] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node fv-az1755-505 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
