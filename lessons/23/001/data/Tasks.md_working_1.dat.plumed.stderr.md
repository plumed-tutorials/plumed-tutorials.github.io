Stderr for source:  Tasks.md_working_1.dat   
Download: [zipped raw stdout](Tasks.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmbietmlfzoi:35063] *** Process received signal ***
[pkrvmbietmlfzoi:35063] Signal: Aborted (6)
[pkrvmbietmlfzoi:35063] Signal code:  (-6)
[pkrvmbietmlfzoi:35063] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe875c45330]
[pkrvmbietmlfzoi:35063] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe875c9eb2c]
[pkrvmbietmlfzoi:35063] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe875c4527e]
[pkrvmbietmlfzoi:35063] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe875c288ff]
[pkrvmbietmlfzoi:35063] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe8760a5ff5]
[pkrvmbietmlfzoi:35063] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe8760bb0da]
[pkrvmbietmlfzoi:35063] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe8760a5a55]
[pkrvmbietmlfzoi:35063] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe8760a5a6f]
[pkrvmbietmlfzoi:35063] [ 8] plumed(+0x13209)[0x56116fcf1209]
[pkrvmbietmlfzoi:35063] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe875c2a1ca]
[pkrvmbietmlfzoi:35063] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe875c2a28b]
[pkrvmbietmlfzoi:35063] [11] plumed(+0x134a5)[0x56116fcf14a5]
[pkrvmbietmlfzoi:35063] *** End of error message ***
</pre>
{% endraw %}
