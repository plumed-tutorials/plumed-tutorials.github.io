Stderr for source:  markdown/inputs.md_working_9.dat   
Download: [zipped raw stdout](inputs.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](inputs.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
[fv-az1755-505:05848] *** Process received signal ***
[fv-az1755-505:05848] Signal: Aborted (6)
[fv-az1755-505:05848] Signal code:  (-6)
[fv-az1755-505:05848] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc51fe45330]
[fv-az1755-505:05848] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc51fe9eb2c]
[fv-az1755-505:05848] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc51fe4527e]
[fv-az1755-505:05848] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc51fe288ff]
[fv-az1755-505:05848] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc5202a5ff5]
[fv-az1755-505:05848] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc5202bb0da]
[fv-az1755-505:05848] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc5202a5a55]
[fv-az1755-505:05848] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc5202a5a6f]
[fv-az1755-505:05848] [ 8] plumed_master(+0x146dd)[0x559e8d7e46dd]
[fv-az1755-505:05848] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc51fe2a1ca]
[fv-az1755-505:05848] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc51fe2a28b]
[fv-az1755-505:05848] [11] plumed_master(+0x15365)[0x559e8d7e5365]
[fv-az1755-505:05848] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
[fv-az1755-505:05846] *** Process received signal ***
[fv-az1755-505:05846] Signal: Aborted (6)
[fv-az1755-505:05846] Signal code:  (-6)
[fv-az1755-505:05846] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f07c0845330]
[fv-az1755-505:05846] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f07c089eb2c]
[fv-az1755-505:05846] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f07c084527e]
[fv-az1755-505:05846] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f07c08288ff]
[fv-az1755-505:05846] [ 4] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
[fv-az1755-505:05847] *** Process received signal ***
[fv-az1755-505:05847] Signal: Aborted (6)
[fv-az1755-505:05847] Signal code:  (-6)
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f07c0ca5ff5]
[fv-az1755-505:05846] [ 5] [fv-az1755-505:05847] [ 0] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f07c0cbb0da]
[fv-az1755-505:05846] [ 6] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1f50e45330]
[fv-az1755-505:05847] [ 1] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f07c0ca5a55]
[fv-az1755-505:05846] [ 7] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1f50e9eb2c]
[fv-az1755-505:05847] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1f50e4527e]
[fv-az1755-505:05847] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f07c0ca5a6f]
[fv-az1755-505:05846] [ 8] plumed_master(+0x146dd)[0x55b1fb5bd6dd]
[fv-az1755-505:05846] [ 9] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1f50e288ff]
[fv-az1755-505:05847] [ 4] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f07c082a1ca]
[fv-az1755-505:05846] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1f512a5ff5]
[fv-az1755-505:05847] [ 5] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f07c082a28b]
[fv-az1755-505:05846] [11] plumed_master(+0x15365)[0x55b1fb5be365]
[fv-az1755-505:05846] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1f512bb0da]
[fv-az1755-505:05847] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1f512a5a55]
[fv-az1755-505:05847] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1f512a5a6f]
[fv-az1755-505:05847] [ 8] plumed_master(+0x146dd)[0x555c312396dd]
[fv-az1755-505:05847] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1f50e2a1ca]
[fv-az1755-505:05847] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1f50e2a28b]
[fv-az1755-505:05847] [11] plumed_master(+0x15365)[0x555c3123a365]
[fv-az1755-505:05847] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 1 with PID 0 on node fv-az1755-505 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
