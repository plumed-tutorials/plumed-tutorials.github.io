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
[fv-az1279-640:06128] *** Process received signal ***
[fv-az1279-640:06128] Signal: Aborted (6)
[fv-az1279-640:06128] Signal code:  (-6)
[fv-az1279-640:06128] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff24e445330]
[fv-az1279-640:06128] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff24e49eb2c]
[fv-az1279-640:06128] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff24e44527e]
[fv-az1279-640:06128] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff24e4288ff]
[fv-az1279-640:06128] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff24e8a5ff5]
[fv-az1279-640:06128] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff24e8bb0da]
[fv-az1279-640:06128] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff24e8a5a55]
[fv-az1279-640:06128] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff24e8a5a6f]
[fv-az1279-640:06128] [ 8] plumed_master(+0x146dd)[0x556dfe5fc6dd]
[fv-az1279-640:06128] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff24e42a1ca]
[fv-az1279-640:06128] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff24e42a28b]
[fv-az1279-640:06128] [11] plumed_master(+0x15365)[0x556dfe5fd365]
[fv-az1279-640:06128] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
[fv-az1279-640:06131] *** Process received signal ***
[fv-az1279-640:06131] Signal: Aborted (6)
[fv-az1279-640:06131] Signal code:  (-6)
[fv-az1279-640:06131] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f970c245330]
[fv-az1279-640:06131] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f970c29eb2c]
[fv-az1279-640:06131] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f970c24527e]
[fv-az1279-640:06131] [ 3] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
/lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f970c2288ff]
[fv-az1279-640:06131] [ 4] [fv-az1279-640:06132] *** Process received signal ***
[fv-az1279-640:06132] Signal: Aborted (6)
[fv-az1279-640:06132] Signal code:  (-6)
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f970c6a5ff5]
[fv-az1279-640:06131] [ 5] [fv-az1279-640:06132] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fad04a45330]
[fv-az1279-640:06132] [ 1] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f970c6bb0da]
[fv-az1279-640:06131] [ 6] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fad04a9eb2c]
[fv-az1279-640:06132] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fad04a4527e]
[fv-az1279-640:06132] [ 3] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f970c6a5a55]
[fv-az1279-640:06131] [ 7] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fad04a288ff]
[fv-az1279-640:06132] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f970c6a5a6f]
[fv-az1279-640:06131] [ 8] plumed_master(+0x146dd)[0x55566f6126dd]
[fv-az1279-640:06131] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fad04ea5ff5]
[fv-az1279-640:06132] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f970c22a1ca]
[fv-az1279-640:06131] [10] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fad04ebb0da]
[fv-az1279-640:06132] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f970c22a28b]
[fv-az1279-640:06131] [11] plumed_master(+0x15365)[0x55566f613365]
[fv-az1279-640:06131] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fad04ea5a55]
[fv-az1279-640:06132] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fad04ea5a6f]
[fv-az1279-640:06132] [ 8] plumed_master(+0x146dd)[0x55f19dd276dd]
[fv-az1279-640:06132] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fad04a2a1ca]
[fv-az1279-640:06132] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fad04a2a28b]
[fv-az1279-640:06132] [11] plumed_master(+0x15365)[0x55f19dd28365]
[fv-az1279-640:06132] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1279-640 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
