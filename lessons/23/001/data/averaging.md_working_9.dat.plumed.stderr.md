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
[pkrvmf6wy0o8zjz:60738] *** Process received signal ***
[pkrvmf6wy0o8zjz:60738] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60738] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60738] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd8d7445330]
[pkrvmf6wy0o8zjz:60738] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd8d749eb2c]
[pkrvmf6wy0o8zjz:60738] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd8d744527e]
[pkrvmf6wy0o8zjz:60738] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd8d74288ff]
[pkrvmf6wy0o8zjz:60738] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd8d78a5ff5]
[pkrvmf6wy0o8zjz:60738] [ 5] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd8d78bb0da]
[pkrvmf6wy0o8zjz:60738] [ 6]   what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=r1g ARG=r1.bias
Maybe a missing space or a typo?
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd8d78a5a55]
[pkrvmf6wy0o8zjz:60738] [ 7] [pkrvmf6wy0o8zjz:60737] *** Process received signal ***
[pkrvmf6wy0o8zjz:60737] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60737] Signal code:  (-6)
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd8d78a5a6f]
[pkrvmf6wy0o8zjz:60738] [ 8] [pkrvmf6wy0o8zjz:60737] [ 0] plumed(+0x13209)[0x5630a90ab209]
[pkrvmf6wy0o8zjz:60738] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd8d742a1ca]
[pkrvmf6wy0o8zjz:60738] [10] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f411ca45330]
[pkrvmf6wy0o8zjz:60737] [ 1] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd8d742a28b]
[pkrvmf6wy0o8zjz:60738] [11] plumed(+0x134a5)[0x5630a90ab4a5]
[pkrvmf6wy0o8zjz:60738] *** End of error message ***
/lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f411ca9eb2c]
[pkrvmf6wy0o8zjz:60737] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f411ca4527e]
[pkrvmf6wy0o8zjz:60737] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f411ca288ff]
[pkrvmf6wy0o8zjz:60737] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f411cea5ff5]
[pkrvmf6wy0o8zjz:60737] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f411cebb0da]
[pkrvmf6wy0o8zjz:60737] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f411cea5a55]
[pkrvmf6wy0o8zjz:60737] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f411cea5a6f]
[pkrvmf6wy0o8zjz:60737] [ 8] plumed(+0x13209)[0x55aefbce8209]
[pkrvmf6wy0o8zjz:60737] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f411ca2a1ca]
[pkrvmf6wy0o8zjz:60737] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f411ca2a28b]
[pkrvmf6wy0o8zjz:60737] [11] plumed(+0x134a5)[0x55aefbce84a5]
[pkrvmf6wy0o8zjz:60737] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node pkrvmf6wy0o8zjz exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
