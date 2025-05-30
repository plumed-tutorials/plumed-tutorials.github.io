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
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61295] *** Process received signal ***
[pkrvmf6wy0o8zjz:61295] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61295] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61296] *** Process received signal ***
[pkrvmf6wy0o8zjz:61296] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61296] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61295] [ 0] [pkrvmf6wy0o8zjz:61296] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb347445330]
[pkrvmf6wy0o8zjz:61295] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9a08645330]
[pkrvmf6wy0o8zjz:61296] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb34749eb2c]
[pkrvmf6wy0o8zjz:61295] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9a0869eb2c]
[pkrvmf6wy0o8zjz:61296] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb34744527e]
[pkrvmf6wy0o8zjz:61295] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb3474288ff]
[pkrvmf6wy0o8zjz:61295] [ 4] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9a0864527e]
[pkrvmf6wy0o8zjz:61296] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9a086288ff]
[pkrvmf6wy0o8zjz:61296] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb3478a5ff5]
[pkrvmf6wy0o8zjz:61295] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9a08aa5ff5]
[pkrvmf6wy0o8zjz:61296] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb3478bb0da]
[pkrvmf6wy0o8zjz:61295] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9a08abb0da]
[pkrvmf6wy0o8zjz:61296] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb3478a5a55]
[pkrvmf6wy0o8zjz:61295] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb3478a5a6f]
[pkrvmf6wy0o8zjz:61295] [ 8] plumed(+0x13209)[0x55867aa7a209]
[pkrvmf6wy0o8zjz:61295] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9a08aa5a55]
[pkrvmf6wy0o8zjz:61296] [ 7] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb34742a1ca]
[pkrvmf6wy0o8zjz:61295] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb34742a28b]
[pkrvmf6wy0o8zjz:61295] [11] plumed(+0x134a5)[0x55867aa7a4a5]
[pkrvmf6wy0o8zjz:61295] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9a08aa5a6f]
[pkrvmf6wy0o8zjz:61296] [ 8] plumed(+0x13209)[0x564a00466209]
[pkrvmf6wy0o8zjz:61296] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9a0862a1ca]
[pkrvmf6wy0o8zjz:61296] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9a0862a28b]
[pkrvmf6wy0o8zjz:61296] [11] plumed(+0x134a5)[0x564a004664a5]
[pkrvmf6wy0o8zjz:61296] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node pkrvmf6wy0o8zjz exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
