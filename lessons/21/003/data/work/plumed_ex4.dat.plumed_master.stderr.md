Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @32 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36674] *** Process received signal ***
[pkrvmbietmlfzoi:36674] Signal: Aborted (6)
[pkrvmbietmlfzoi:36674] Signal code:  (-6)
[pkrvmbietmlfzoi:36674] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7566645330]
[pkrvmbietmlfzoi:36674] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f756669eb2c]
[pkrvmbietmlfzoi:36674] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f756664527e]
[pkrvmbietmlfzoi:36674] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f75666288ff]
[pkrvmbietmlfzoi:36674] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7566aa5ff5]
[pkrvmbietmlfzoi:36674] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7566abb0da]
[pkrvmbietmlfzoi:36674] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7566aa5a55]
[pkrvmbietmlfzoi:36674] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7566aa5a6f]
[pkrvmbietmlfzoi:36674] [ 8] plumed_master(+0x146dd)[0x55dcbc7696dd]
[pkrvmbietmlfzoi:36674] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f756662a1ca]
[pkrvmbietmlfzoi:36674] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f756662a28b]
[pkrvmbietmlfzoi:36674] [11] plumed_master(+0x15365)[0x55dcbc76a365]
[pkrvmbietmlfzoi:36674] *** End of error message ***
</pre>
{% endraw %}
