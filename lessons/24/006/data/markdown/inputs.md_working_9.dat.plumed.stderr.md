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
[fv-az1755-505:05805] *** Process received signal ***
[fv-az1755-505:05805] Signal: Aborted (6)
[fv-az1755-505:05805] Signal code:  (-6)
[fv-az1755-505:05805] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f95f9a45330]
[fv-az1755-505:05805] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f95f9a9eb2c]
[fv-az1755-505:05805] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f95f9a4527e]
[fv-az1755-505:05805] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f95f9a288ff]
[fv-az1755-505:05805] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f95f9ea5ff5]
[fv-az1755-505:05805] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f95f9ebb0da]
[fv-az1755-505:05805] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f95f9ea5a55]
[fv-az1755-505:05805] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f95f9ea5a6f]
[fv-az1755-505:05805] [ 8] plumed(+0x13209)[0x55e316ebf209]
[fv-az1755-505:05805] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f95f9a2a1ca]
[fv-az1755-505:05805] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f95f9a2a28b]
[fv-az1755-505:05805] [11] plumed(+0x134a5)[0x55e316ebf4a5]
[fv-az1755-505:05805] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[fv-az1755-505:05804] *** Process received signal ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
[fv-az1755-505:05804] Signal: Aborted (6)
[fv-az1755-505:05804] Signal code:  (-6)
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[fv-az1755-505:05804] [ 0] [fv-az1755-505:05803] *** Process received signal ***
[fv-az1755-505:05803] Signal: Aborted (6)
[fv-az1755-505:05803] Signal code:  (-6)
[fv-az1755-505:05803] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe981845330]
[fv-az1755-505:05804] [ 1] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcf07e45330]
[fv-az1755-505:05803] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe98189eb2c]
[fv-az1755-505:05804] [ 2] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcf07e9eb2c]
[fv-az1755-505:05803] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe98184527e]
[fv-az1755-505:05804] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe9818288ff]
[fv-az1755-505:05804] [ 4] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcf07e4527e]
[fv-az1755-505:05803] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcf07e288ff]
[fv-az1755-505:05803] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe981ca5ff5]
[fv-az1755-505:05804] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcf082a5ff5]
[fv-az1755-505:05803] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe981cbb0da]
[fv-az1755-505:05804] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcf082bb0da]
[fv-az1755-505:05803] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe981ca5a55]
[fv-az1755-505:05804] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe981ca5a6f]
[fv-az1755-505:05804] [ 8] plumed(+0x13209)[0x5581a7ee2209]
/lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcf082a5a55]
[fv-az1755-505:05803] [ 7] [fv-az1755-505:05804] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcf082a5a6f]
[fv-az1755-505:05803] [ 8] plumed(+0x13209)[0x55770d6f1209]
[fv-az1755-505:05803] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe98182a1ca]
[fv-az1755-505:05804] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe98182a28b]
[fv-az1755-505:05804] [11] plumed(+0x134a5)[0x5581a7ee24a5]
[fv-az1755-505:05804] *** End of error message ***
/lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcf07e2a1ca]
[fv-az1755-505:05803] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcf07e2a28b]
[fv-az1755-505:05803] [11] plumed(+0x134a5)[0x55770d6f14a5]
[fv-az1755-505:05803] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 0 with PID 0 on node fv-az1755-505 exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
