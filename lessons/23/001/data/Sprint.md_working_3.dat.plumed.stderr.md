Stderr for source:  Sprint.md_working_3.dat   
Download: [zipped raw stdout](Sprint.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label ss : keyword MATRIX is compulsory for this action
[pkrvmbietmlfzoi:35230] *** Process received signal ***
[pkrvmbietmlfzoi:35230] Signal: Aborted (6)
[pkrvmbietmlfzoi:35230] Signal code:  (-6)
[pkrvmbietmlfzoi:35230] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f12dc845330]
[pkrvmbietmlfzoi:35230] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f12dc89eb2c]
[pkrvmbietmlfzoi:35230] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f12dc84527e]
[pkrvmbietmlfzoi:35230] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f12dc8288ff]
[pkrvmbietmlfzoi:35230] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f12dcca5ff5]
[pkrvmbietmlfzoi:35230] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f12dccbb0da]
[pkrvmbietmlfzoi:35230] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f12dcca5a55]
[pkrvmbietmlfzoi:35230] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f12dcca5a6f]
[pkrvmbietmlfzoi:35230] [ 8] plumed(+0x13209)[0x55c721f51209]
[pkrvmbietmlfzoi:35230] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f12dc82a1ca]
[pkrvmbietmlfzoi:35230] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f12dc82a28b]
[pkrvmbietmlfzoi:35230] [11] plumed(+0x134a5)[0x55c721f514a5]
[pkrvmbietmlfzoi:35230] *** End of error message ***
</pre>
{% endraw %}
