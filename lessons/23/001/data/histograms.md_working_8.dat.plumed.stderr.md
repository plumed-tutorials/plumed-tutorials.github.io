Stderr for source:  histograms.md_working_8.dat   
Download: [zipped raw stdout](histograms.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61046] *** Process received signal ***
[pkrvmf6wy0o8zjz:61046] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61046] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61046] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa7cf645330]
[pkrvmf6wy0o8zjz:61046] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa7cf69eb2c]
[pkrvmf6wy0o8zjz:61046] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa7cf64527e]
[pkrvmf6wy0o8zjz:61046] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa7cf6288ff]
[pkrvmf6wy0o8zjz:61046] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa7cfaa5ff5]
[pkrvmf6wy0o8zjz:61046] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa7cfabb0da]
[pkrvmf6wy0o8zjz:61046] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa7cfaa5a55]
[pkrvmf6wy0o8zjz:61046] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa7cfaa5a6f]
[pkrvmf6wy0o8zjz:61046] [ 8] plumed(+0x13209)[0x562e52d7d209]
[pkrvmf6wy0o8zjz:61046] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa7cf62a1ca]
[pkrvmf6wy0o8zjz:61046] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa7cf62a28b]
[pkrvmf6wy0o8zjz:61046] [11] plumed(+0x134a5)[0x562e52d7d4a5]
[pkrvmf6wy0o8zjz:61046] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61045] *** Process received signal ***
[pkrvmf6wy0o8zjz:61045] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61045] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61045] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8ea6045330]
[pkrvmf6wy0o8zjz:61045] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8ea609eb2c]
[pkrvmf6wy0o8zjz:61045] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8ea604527e]
[pkrvmf6wy0o8zjz:61045] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8ea60288ff]
[pkrvmf6wy0o8zjz:61045] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8ea64a5ff5]
[pkrvmf6wy0o8zjz:61045] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8ea64bb0da]
[pkrvmf6wy0o8zjz:61045] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8ea64a5a55]
[pkrvmf6wy0o8zjz:61045] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8ea64a5a6f]
[pkrvmf6wy0o8zjz:61045] [ 8] plumed(+0x13209)[0x55d21758a209]
[pkrvmf6wy0o8zjz:61045] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8ea602a1ca]
[pkrvmf6wy0o8zjz:61045] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8ea602a28b]
[pkrvmf6wy0o8zjz:61045] [11] plumed(+0x134a5)[0x55d21758a4a5]
[pkrvmf6wy0o8zjz:61045] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node pkrvmf6wy0o8zjz exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
