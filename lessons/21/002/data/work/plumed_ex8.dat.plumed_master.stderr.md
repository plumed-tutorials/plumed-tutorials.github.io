Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @46 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36908] *** Process received signal ***
[pkrvmbietmlfzoi:36908] Signal: Aborted (6)
[pkrvmbietmlfzoi:36908] Signal code:  (-6)
[pkrvmbietmlfzoi:36908] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faf1e445330]
[pkrvmbietmlfzoi:36908] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faf1e49eb2c]
[pkrvmbietmlfzoi:36908] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faf1e44527e]
[pkrvmbietmlfzoi:36908] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faf1e4288ff]
[pkrvmbietmlfzoi:36908] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faf1e8a5ff5]
[pkrvmbietmlfzoi:36908] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faf1e8bb0da]
[pkrvmbietmlfzoi:36908] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faf1e8a5a55]
[pkrvmbietmlfzoi:36908] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faf1e8a5a6f]
[pkrvmbietmlfzoi:36908] [ 8] plumed_master(+0x146dd)[0x55dd86ba36dd]
[pkrvmbietmlfzoi:36908] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faf1e42a1ca]
[pkrvmbietmlfzoi:36908] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faf1e42a28b]
[pkrvmbietmlfzoi:36908] [11] plumed_master(+0x15365)[0x55dd86ba4365]
[pkrvmbietmlfzoi:36908] *** End of error message ***
</pre>
{% endraw %}
