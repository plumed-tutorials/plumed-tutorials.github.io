Stderr for source:  contactMatrix.md_working_1.dat   
Download: [zipped raw stdout](contactMatrix.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[pkrvmbietmlfzoi:34910] *** Process received signal ***
[pkrvmbietmlfzoi:34910] Signal: Aborted (6)
[pkrvmbietmlfzoi:34910] Signal code:  (-6)
[pkrvmbietmlfzoi:34910] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9f20445330]
[pkrvmbietmlfzoi:34910] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9f2049eb2c]
[pkrvmbietmlfzoi:34910] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9f2044527e]
[pkrvmbietmlfzoi:34910] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9f204288ff]
[pkrvmbietmlfzoi:34910] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9f208a5ff5]
[pkrvmbietmlfzoi:34910] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9f208bb0da]
[pkrvmbietmlfzoi:34910] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9f208a5a55]
[pkrvmbietmlfzoi:34910] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9f208a5a6f]
[pkrvmbietmlfzoi:34910] [ 8] plumed(+0x13209)[0x563a8660c209]
[pkrvmbietmlfzoi:34910] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9f2042a1ca]
[pkrvmbietmlfzoi:34910] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9f2042a28b]
[pkrvmbietmlfzoi:34910] [11] plumed(+0x134a5)[0x563a8660c4a5]
[pkrvmbietmlfzoi:34910] *** End of error message ***
</pre>
{% endraw %}
