Stderr for source:  markdown/inputs.md_working_9.dat   
Download: [zipped raw stdout](inputs.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](inputs.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[fv-az1279-640:06085] *** Process received signal ***
[fv-az1279-640:06085] Signal: Aborted (6)
[fv-az1279-640:06085] Signal code:  (-6)
[fv-az1279-640:06085] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1325c45330]
[fv-az1279-640:06085] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1325c9eb2c]
[fv-az1279-640:06085] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1325c4527e]
[fv-az1279-640:06085] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1325c288ff]
[fv-az1279-640:06085] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f13260a5ff5]
[fv-az1279-640:06085] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f13260bb0da]
[fv-az1279-640:06085] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f13260a5a55]
[fv-az1279-640:06085] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f13260a5a6f]
[fv-az1279-640:06085] [ 8] plumed(+0x13209)[0x559cbc459209]
[fv-az1279-640:06085] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1325c2a1ca]
[fv-az1279-640:06085] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1325c2a28b]
[fv-az1279-640:06085] [11] plumed(+0x134a5)[0x559cbc4594a5]
[fv-az1279-640:06085] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[fv-az1279-640:06087] *** Process received signal ***
[fv-az1279-640:06087] Signal: Aborted (6)
[fv-az1279-640:06087] Signal code:  (-6)
[fv-az1279-640:06087] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdaf3c45330]
[fv-az1279-640:06087] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdaf3c9eb2c]
[fv-az1279-640:06087] [ 2] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
/lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdaf3c4527e]
[fv-az1279-640:06087] [ 3]   what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[fv-az1279-640:06086] *** Process received signal ***
[fv-az1279-640:06086] Signal: Aborted (6)
[fv-az1279-640:06086] Signal code:  (-6)
/lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdaf3c288ff]
[fv-az1279-640:06087] [ 4] [fv-az1279-640:06086] [ 0] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdaf40a5ff5]
[fv-az1279-640:06087] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb746c45330]
[fv-az1279-640:06086] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb746c9eb2c]
[fv-az1279-640:06086] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdaf40bb0da]
[fv-az1279-640:06087] [ 6] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb746c4527e]
[fv-az1279-640:06086] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb746c288ff]
[fv-az1279-640:06086] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdaf40a5a55]
[fv-az1279-640:06087] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb7470a5ff5]
[fv-az1279-640:06086] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdaf40a5a6f]
[fv-az1279-640:06087] [ 8] plumed(+0x13209)[0x55f852fe4209]
[fv-az1279-640:06087] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdaf3c2a1ca]
[fv-az1279-640:06087] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb7470bb0da]
[fv-az1279-640:06086] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdaf3c2a28b]
[fv-az1279-640:06087] [11] plumed(+0x134a5)[0x55f852fe44a5]
[fv-az1279-640:06087] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb7470a5a55]
[fv-az1279-640:06086] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb7470a5a6f]
[fv-az1279-640:06086] [ 8] plumed(+0x13209)[0x5573c63c2209]
[fv-az1279-640:06086] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb746c2a1ca]
[fv-az1279-640:06086] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb746c2a28b]
[fv-az1279-640:06086] [11] plumed(+0x134a5)[0x5573c63c24a5]
[fv-az1279-640:06086] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 2 with PID 0 on node fv-az1279-640 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
