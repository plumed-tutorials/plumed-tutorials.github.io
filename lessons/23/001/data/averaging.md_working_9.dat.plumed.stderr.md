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
[pkrvmf6wy0o8zjz:60988] *** Process received signal ***
[pkrvmf6wy0o8zjz:60988] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60988] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60988] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0c2a245330]
[pkrvmf6wy0o8zjz:60988] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0c2a29eb2c]
[pkrvmf6wy0o8zjz:60988] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0c2a24527e]
[pkrvmf6wy0o8zjz:60988] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0c2a2288ff]
[pkrvmf6wy0o8zjz:60988] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0c2a6a5ff5]
[pkrvmf6wy0o8zjz:60988] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0c2a6bb0da]
[pkrvmf6wy0o8zjz:60988] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0c2a6a5a55]
[pkrvmf6wy0o8zjz:60988] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0c2a6a5a6f]
[pkrvmf6wy0o8zjz:60988] [ 8] plumed(+0x13209)[0x556d48e8b209]
[pkrvmf6wy0o8zjz:60988] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0c2a22a1ca]
[pkrvmf6wy0o8zjz:60988] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0c2a22a28b]
[pkrvmf6wy0o8zjz:60988] [11] plumed(+0x134a5)[0x556d48e8b4a5]
[pkrvmf6wy0o8zjz:60988] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:60989] *** Process received signal ***
[pkrvmf6wy0o8zjz:60989] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60989] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60989] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc237845330]
[pkrvmf6wy0o8zjz:60989] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc23789eb2c]
[pkrvmf6wy0o8zjz:60989] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc23784527e]
[pkrvmf6wy0o8zjz:60989] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc2378288ff]
[pkrvmf6wy0o8zjz:60989] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc237ca5ff5]
[pkrvmf6wy0o8zjz:60989] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc237cbb0da]
[pkrvmf6wy0o8zjz:60989] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc237ca5a55]
[pkrvmf6wy0o8zjz:60989] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc237ca5a6f]
[pkrvmf6wy0o8zjz:60989] [ 8] plumed(+0x13209)[0x55689f733209]
[pkrvmf6wy0o8zjz:60989] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc23782a1ca]
[pkrvmf6wy0o8zjz:60989] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc23782a28b]
[pkrvmf6wy0o8zjz:60989] [11] plumed(+0x134a5)[0x55689f7334a5]
[pkrvmf6wy0o8zjz:60989] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node pkrvmf6wy0o8zjz exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
