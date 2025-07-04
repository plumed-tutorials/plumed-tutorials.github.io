Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmbietmlfzoi:34717] *** Process received signal ***
[pkrvmbietmlfzoi:34717] Signal: Aborted (6)
[pkrvmbietmlfzoi:34717] Signal code:  (-6)
[pkrvmbietmlfzoi:34717] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcabc645330]
[pkrvmbietmlfzoi:34717] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcabc69eb2c]
[pkrvmbietmlfzoi:34717] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcabc64527e]
[pkrvmbietmlfzoi:34717] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcabc6288ff]
[pkrvmbietmlfzoi:34717] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcabcaa5ff5]
[pkrvmbietmlfzoi:34717] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcabcabb0da]
[pkrvmbietmlfzoi:34717] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcabcaa5a55]
[pkrvmbietmlfzoi:34717] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcabcaa5a6f]
[pkrvmbietmlfzoi:34717] [ 8] plumed(+0x13209)[0x564792a3d209]
[pkrvmbietmlfzoi:34717] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcabc62a1ca]
[pkrvmbietmlfzoi:34717] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcabc62a28b]
[pkrvmbietmlfzoi:34717] [11] plumed(+0x134a5)[0x564792a3d4a5]
[pkrvmbietmlfzoi:34717] *** End of error message ***
</pre>
{% endraw %}
