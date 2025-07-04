Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @37 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36621] *** Process received signal ***
[pkrvmbietmlfzoi:36621] Signal: Aborted (6)
[pkrvmbietmlfzoi:36621] Signal code:  (-6)
[pkrvmbietmlfzoi:36621] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbd8b045330]
[pkrvmbietmlfzoi:36621] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbd8b09eb2c]
[pkrvmbietmlfzoi:36621] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbd8b04527e]
[pkrvmbietmlfzoi:36621] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbd8b0288ff]
[pkrvmbietmlfzoi:36621] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbd8b4a5ff5]
[pkrvmbietmlfzoi:36621] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbd8b4bb0da]
[pkrvmbietmlfzoi:36621] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbd8b4a5a55]
[pkrvmbietmlfzoi:36621] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbd8b4a5a6f]
[pkrvmbietmlfzoi:36621] [ 8] plumed_master(+0x146dd)[0x5555910866dd]
[pkrvmbietmlfzoi:36621] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbd8b02a1ca]
[pkrvmbietmlfzoi:36621] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbd8b02a28b]
[pkrvmbietmlfzoi:36621] [11] plumed_master(+0x15365)[0x555591087365]
[pkrvmbietmlfzoi:36621] *** End of error message ***
</pre>
{% endraw %}
