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
[fv-az1315-757:08026] *** Process received signal ***
[fv-az1315-757:08026] Signal: Aborted (6)
[fv-az1315-757:08026] Signal code:  (-6)
[fv-az1315-757:08026] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd51e845330]
[fv-az1315-757:08026] [ 1] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1c ARG=d1
Maybe a missing space or a typo?/lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd51e89eb2c]
[fv-az1315-757:08026] [ 2]
[fv-az1315-757:08025] *** Process received signal ***
[fv-az1315-757:08025] Signal: Aborted (6)
[fv-az1315-757:08025] Signal code:  (-6)
/lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd51e84527e]
[fv-az1315-757:08026] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd51e8288ff]
[fv-az1315-757:08026] [ 4] [fv-az1315-757:08025] [ 0] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd51eca5ff5]
[fv-az1315-757:08026] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6cbaa45330]
[fv-az1315-757:08025] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6cbaa9eb2c]
[fv-az1315-757:08025] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd51ecbb0da]
[fv-az1315-757:08026] [ 6] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6cbaa4527e]
[fv-az1315-757:08025] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd51eca5a55]
[fv-az1315-757:08026] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd51eca5a6f]
[fv-az1315-757:08026] [ 8] plumed(+0x13209)[0x55ff46806209]
[fv-az1315-757:08026] [ 9] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6cbaa288ff]
[fv-az1315-757:08025] [ 4] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd51e82a1ca]
[fv-az1315-757:08026] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd51e82a28b]
[fv-az1315-757:08026] [11] plumed(+0x134a5)[0x55ff468064a5]
[fv-az1315-757:08026] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6cbaea5ff5]
[fv-az1315-757:08025] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6cbaebb0da]
[fv-az1315-757:08025] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6cbaea5a55]
[fv-az1315-757:08025] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6cbaea5a6f]
[fv-az1315-757:08025] [ 8] plumed(+0x13209)[0x55cfd1e8c209]
[fv-az1315-757:08025] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6cbaa2a1ca]
[fv-az1315-757:08025] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6cbaa2a28b]
[fv-az1315-757:08025] [11] plumed(+0x134a5)[0x55cfd1e8c4a5]
[fv-az1315-757:08025] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1315-757 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
