Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @12 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36827] *** Process received signal ***
[pkrvmbietmlfzoi:36827] Signal: Aborted (6)
[pkrvmbietmlfzoi:36827] Signal code:  (-6)
[pkrvmbietmlfzoi:36827] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efc75e45330]
[pkrvmbietmlfzoi:36827] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efc75e9eb2c]
[pkrvmbietmlfzoi:36827] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efc75e4527e]
[pkrvmbietmlfzoi:36827] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efc75e288ff]
[pkrvmbietmlfzoi:36827] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efc762a5ff5]
[pkrvmbietmlfzoi:36827] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efc762bb0da]
[pkrvmbietmlfzoi:36827] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efc762a5a55]
[pkrvmbietmlfzoi:36827] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efc762a5a6f]
[pkrvmbietmlfzoi:36827] [ 8] plumed_master(+0x146dd)[0x56294ec516dd]
[pkrvmbietmlfzoi:36827] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efc75e2a1ca]
[pkrvmbietmlfzoi:36827] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efc75e2a28b]
[pkrvmbietmlfzoi:36827] [11] plumed_master(+0x15365)[0x56294ec52365]
[pkrvmbietmlfzoi:36827] *** End of error message ***
</pre>
{% endraw %}
