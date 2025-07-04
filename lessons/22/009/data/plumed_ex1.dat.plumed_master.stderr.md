Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[pkrvmbietmlfzoi:35466] *** Process received signal ***
[pkrvmbietmlfzoi:35466] Signal: Aborted (6)
[pkrvmbietmlfzoi:35466] Signal code:  (-6)
[pkrvmbietmlfzoi:35466] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f78e7e45330]
[pkrvmbietmlfzoi:35466] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f78e7e9eb2c]
[pkrvmbietmlfzoi:35466] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f78e7e4527e]
[pkrvmbietmlfzoi:35466] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f78e7e288ff]
[pkrvmbietmlfzoi:35466] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f78e82a5ff5]
[pkrvmbietmlfzoi:35466] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f78e82bb0da]
[pkrvmbietmlfzoi:35466] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f78e82a5a55]
[pkrvmbietmlfzoi:35466] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f78e82a5a6f]
[pkrvmbietmlfzoi:35466] [ 8] plumed_master(+0x146dd)[0x557d6b0ec6dd]
[pkrvmbietmlfzoi:35466] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f78e7e2a1ca]
[pkrvmbietmlfzoi:35466] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f78e7e2a28b]
[pkrvmbietmlfzoi:35466] [11] plumed_master(+0x15365)[0x557d6b0ed365]
[pkrvmbietmlfzoi:35466] *** End of error message ***
</pre>
{% endraw %}
