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
[pkrvmf6wy0o8zjz:59588] *** Process received signal ***
[pkrvmf6wy0o8zjz:59588] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59588] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59588] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0c22845330]
[pkrvmf6wy0o8zjz:59588] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0c2289eb2c]
[pkrvmf6wy0o8zjz:59588] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0c2284527e]
[pkrvmf6wy0o8zjz:59588] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0c228288ff]
[pkrvmf6wy0o8zjz:59588] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0c22ca5ff5]
[pkrvmf6wy0o8zjz:59588] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0c22cbb0da]
[pkrvmf6wy0o8zjz:59588] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0c22ca5a55]
[pkrvmf6wy0o8zjz:59588] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0c22ca5a6f]
[pkrvmf6wy0o8zjz:59588] [ 8] plumed_master(+0x146dd)[0x557066c8f6dd]
[pkrvmf6wy0o8zjz:59588] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0c2282a1ca]
[pkrvmf6wy0o8zjz:59588] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0c2282a28b]
[pkrvmf6wy0o8zjz:59588] [11] plumed_master(+0x15365)[0x557066c90365]
[pkrvmf6wy0o8zjz:59588] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @3 : keyword WALKERS_N could not be read correctly
[pkrvmf6wy0o8zjz:59586] *** Process received signal ***
[pkrvmf6wy0o8zjz:59586] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59586] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59587] *** Process received signal ***
[pkrvmf6wy0o8zjz:59587] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59587] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59586] [ 0] [pkrvmf6wy0o8zjz:59587] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd09d245330]
[pkrvmf6wy0o8zjz:59587] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1703c45330]
[pkrvmf6wy0o8zjz:59586] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd09d29eb2c]
[pkrvmf6wy0o8zjz:59587] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1703c9eb2c]
[pkrvmf6wy0o8zjz:59586] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd09d24527e]
[pkrvmf6wy0o8zjz:59587] [ 3] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1703c4527e]
[pkrvmf6wy0o8zjz:59586] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd09d2288ff]
[pkrvmf6wy0o8zjz:59587] [ 4] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1703c288ff]
[pkrvmf6wy0o8zjz:59586] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd09d6a5ff5]
[pkrvmf6wy0o8zjz:59587] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f17040a5ff5]
[pkrvmf6wy0o8zjz:59586] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd09d6bb0da]
[pkrvmf6wy0o8zjz:59587] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f17040bb0da]
[pkrvmf6wy0o8zjz:59586] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd09d6a5a55]
[pkrvmf6wy0o8zjz:59587] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f17040a5a55]
[pkrvmf6wy0o8zjz:59586] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd09d6a5a6f]
[pkrvmf6wy0o8zjz:59587] [ 8] plumed_master(+0x146dd)[0x55a26d7956dd]
[pkrvmf6wy0o8zjz:59587] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f17040a5a6f]
[pkrvmf6wy0o8zjz:59586] [ 8] plumed_master(+0x146dd)[0x557ca30d36dd]
[pkrvmf6wy0o8zjz:59586] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd09d22a1ca]
[pkrvmf6wy0o8zjz:59587] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd09d22a28b]
[pkrvmf6wy0o8zjz:59587] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1703c2a1ca]
[pkrvmf6wy0o8zjz:59586] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1703c2a28b]
[pkrvmf6wy0o8zjz:59586] [11] [11] plumed_master(+0x15365)[0x55a26d796365]
plumed_master(+0x15365)[0x557ca30d4365]
[pkrvmf6wy0o8zjz:59586] *** End of error message ***
[pkrvmf6wy0o8zjz:59587] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 2 with PID 0 on node pkrvmf6wy0o8zjz exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
