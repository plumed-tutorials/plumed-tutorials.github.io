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
[pkrvmbietmlfzoi:35584] *** Process received signal ***
[pkrvmbietmlfzoi:35584] Signal: Aborted (6)
[pkrvmbietmlfzoi:35584] Signal code:  (-6)
[pkrvmbietmlfzoi:35584] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f768c445330]
[pkrvmbietmlfzoi:35584] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f768c49eb2c]
[pkrvmbietmlfzoi:35584] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f768c44527e]
[pkrvmbietmlfzoi:35584] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f768c4288ff]
[pkrvmbietmlfzoi:35584] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f768c8a5ff5]
[pkrvmbietmlfzoi:35584] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f768c8bb0da]
[pkrvmbietmlfzoi:35584] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f768c8a5a55]
[pkrvmbietmlfzoi:35584] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f768c8a5a6f]
[pkrvmbietmlfzoi:35584] [ 8] plumed(+0x13209)[0x55b5e7f13209]
[pkrvmbietmlfzoi:35584] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f768c42a1ca]
[pkrvmbietmlfzoi:35584] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f768c42a28b]
[pkrvmbietmlfzoi:35584] [11] plumed(+0x134a5)[0x55b5e7f134a5]
[pkrvmbietmlfzoi:35584] *** End of error message ***
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[pkrvmbietmlfzoi:35582] *** Process received signal ***
[pkrvmbietmlfzoi:35582] Signal: Aborted (6)
[pkrvmbietmlfzoi:35582] Signal code:  (-6)
[pkrvmbietmlfzoi:35582] [ 0] terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
/lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4508445330]
[pkrvmbietmlfzoi:35582] [ 1]   what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label @2 : keyword WALKERS_N could not be read correctly
[pkrvmbietmlfzoi:35583] *** Process received signal ***
[pkrvmbietmlfzoi:35583] Signal: Aborted (6)
[pkrvmbietmlfzoi:35583] Signal code:  (-6)
/lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f450849eb2c]
[pkrvmbietmlfzoi:35582] [ 2] [pkrvmbietmlfzoi:35583] [ 0] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f450844527e]
[pkrvmbietmlfzoi:35582] [ 3] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f32dc645330]
[pkrvmbietmlfzoi:35583] [ 1] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f45084288ff]
[pkrvmbietmlfzoi:35582] [ 4] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f32dc69eb2c]
[pkrvmbietmlfzoi:35583] [ 2] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f45088a5ff5]
[pkrvmbietmlfzoi:35582] [ 5] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f32dc64527e]
[pkrvmbietmlfzoi:35583] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f32dc6288ff]
[pkrvmbietmlfzoi:35583] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f45088bb0da]
[pkrvmbietmlfzoi:35582] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f32dcaa5ff5]
[pkrvmbietmlfzoi:35583] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f45088a5a55]
[pkrvmbietmlfzoi:35582] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f32dcabb0da]
[pkrvmbietmlfzoi:35583] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f45088a5a6f]
[pkrvmbietmlfzoi:35582] [ 8] plumed(+0x13209)[0x55ac77248209]
[pkrvmbietmlfzoi:35582] [ 9] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f32dcaa5a55]
[pkrvmbietmlfzoi:35583] [ 7] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f450842a1ca]
[pkrvmbietmlfzoi:35582] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f450842a28b]
[pkrvmbietmlfzoi:35582] [11] plumed(+0x134a5)[0x55ac772484a5]
[pkrvmbietmlfzoi:35582] *** End of error message ***
/lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f32dcaa5a6f]
[pkrvmbietmlfzoi:35583] [ 8] plumed(+0x13209)[0x55f7c022e209]
[pkrvmbietmlfzoi:35583] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f32dc62a1ca]
[pkrvmbietmlfzoi:35583] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f32dc62a28b]
[pkrvmbietmlfzoi:35583] [11] plumed(+0x134a5)[0x55f7c022e4a5]
[pkrvmbietmlfzoi:35583] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
--------------------------------------------------------------------------
--------------------------------------------------------------------------
mpirun noticed that process rank 2 with PID 0 on node pkrvmbietmlfzoi exited on signal 6 (Aborted).
--------------------------------------------------------------------------
</pre>
{% endraw %}
