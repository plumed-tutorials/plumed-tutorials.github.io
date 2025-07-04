Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @65 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36399] *** Process received signal ***
[pkrvmbietmlfzoi:36399] Signal: Aborted (6)
[pkrvmbietmlfzoi:36399] Signal code:  (-6)
[pkrvmbietmlfzoi:36399] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1bf7e45330]
[pkrvmbietmlfzoi:36399] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1bf7e9eb2c]
[pkrvmbietmlfzoi:36399] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1bf7e4527e]
[pkrvmbietmlfzoi:36399] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1bf7e288ff]
[pkrvmbietmlfzoi:36399] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1bf82a5ff5]
[pkrvmbietmlfzoi:36399] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1bf82bb0da]
[pkrvmbietmlfzoi:36399] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1bf82a5a55]
[pkrvmbietmlfzoi:36399] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1bf82a5a6f]
[pkrvmbietmlfzoi:36399] [ 8] plumed_master(+0x146dd)[0x5651ccdef6dd]
[pkrvmbietmlfzoi:36399] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1bf7e2a1ca]
[pkrvmbietmlfzoi:36399] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1bf7e2a28b]
[pkrvmbietmlfzoi:36399] [11] plumed_master(+0x15365)[0x5651ccdf0365]
[pkrvmbietmlfzoi:36399] *** End of error message ***
</pre>
{% endraw %}
