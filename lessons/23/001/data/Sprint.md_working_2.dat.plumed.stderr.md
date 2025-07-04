Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[pkrvmbietmlfzoi:35186] *** Process received signal ***
[pkrvmbietmlfzoi:35186] Signal: Aborted (6)
[pkrvmbietmlfzoi:35186] Signal code:  (-6)
[pkrvmbietmlfzoi:35186] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc914045330]
[pkrvmbietmlfzoi:35186] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc91409eb2c]
[pkrvmbietmlfzoi:35186] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc91404527e]
[pkrvmbietmlfzoi:35186] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc9140288ff]
[pkrvmbietmlfzoi:35186] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc9144a5ff5]
[pkrvmbietmlfzoi:35186] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc9144bb0da]
[pkrvmbietmlfzoi:35186] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc9144a5a55]
[pkrvmbietmlfzoi:35186] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc9144a5a6f]
[pkrvmbietmlfzoi:35186] [ 8] plumed(+0x13209)[0x5638b63fd209]
[pkrvmbietmlfzoi:35186] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc91402a1ca]
[pkrvmbietmlfzoi:35186] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc91402a28b]
[pkrvmbietmlfzoi:35186] [11] plumed(+0x134a5)[0x5638b63fd4a5]
[pkrvmbietmlfzoi:35186] *** End of error message ***
</pre>
{% endraw %}
