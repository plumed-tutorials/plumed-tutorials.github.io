Stderr for source:  histograms.md_working_7.dat   
Download: [zipped raw stdout](histograms.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_7.dat.plumed.stderr.txt.zip) 
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
[runnervm3jyl0:49057] *** Process received signal ***
[runnervm3jyl0:49057] Signal: Aborted (6)
[runnervm3jyl0:49057] Signal code:  (-6)
[runnervm3jyl0:49057] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff284445330]
[runnervm3jyl0:49057] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff28449eb2c]
[runnervm3jyl0:49057] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff28444527e]
[runnervm3jyl0:49057] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff2844288ff]
[runnervm3jyl0:49057] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff2848a5ff5]
[runnervm3jyl0:49057] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff2848bb0da]
[runnervm3jyl0:49057] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff2848a5a55]
[runnervm3jyl0:49057] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff2848a5a6f]
[runnervm3jyl0:49057] [ 8] plumed(+0x13209)[0x55b07adf9209]
[runnervm3jyl0:49057] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff28442a1ca]
[runnervm3jyl0:49057] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff28442a28b]
[runnervm3jyl0:49057] [11] plumed(+0x134a5)[0x55b07adf94a5]
[runnervm3jyl0:49057] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?
[runnervm3jyl0:49058] *** Process received signal ***
[runnervm3jyl0:49058] Signal: Aborted (6)
[runnervm3jyl0:49058] Signal code:  (-6)
[runnervm3jyl0:49058] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9d4b645330]
[runnervm3jyl0:49058] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9d4b69eb2c]
[runnervm3jyl0:49058] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9d4b64527e]
[runnervm3jyl0:49058] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9d4b6288ff]
[runnervm3jyl0:49058] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9d4baa5ff5]
[runnervm3jyl0:49058] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9d4babb0da]
[runnervm3jyl0:49058] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9d4baa5a55]
[runnervm3jyl0:49058] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9d4baa5a6f]
[runnervm3jyl0:49058] [ 8] plumed(+0x13209)[0x560246ea4209]
[runnervm3jyl0:49058] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9d4b62a1ca]
[runnervm3jyl0:49058] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9d4b62a28b]
[runnervm3jyl0:49058] [11] plumed(+0x134a5)[0x560246ea44a5]
[runnervm3jyl0:49058] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node runnervm3jyl0 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
