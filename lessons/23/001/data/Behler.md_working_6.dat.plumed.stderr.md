Stderr for source:  Behler.md_working_6.dat   
Download: [zipped raw stdout](Behler.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:36130] *** Process received signal ***
[pkrvmbietmlfzoi:36130] Signal: Aborted (6)
[pkrvmbietmlfzoi:36130] Signal code:  (-6)
[pkrvmbietmlfzoi:36130] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb202445330]
[pkrvmbietmlfzoi:36130] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb20249eb2c]
[pkrvmbietmlfzoi:36130] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb20244527e]
[pkrvmbietmlfzoi:36130] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb2024288ff]
[pkrvmbietmlfzoi:36130] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb2028a5ff5]
[pkrvmbietmlfzoi:36130] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb2028bb0da]
[pkrvmbietmlfzoi:36130] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb2028a5a55]
[pkrvmbietmlfzoi:36130] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb2028a5a6f]
[pkrvmbietmlfzoi:36130] [ 8] plumed(+0x13209)[0x55ce0e536209]
[pkrvmbietmlfzoi:36130] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb20242a1ca]
[pkrvmbietmlfzoi:36130] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb20242a28b]
[pkrvmbietmlfzoi:36130] [11] plumed(+0x134a5)[0x55ce0e5364a5]
[pkrvmbietmlfzoi:36130] *** End of error message ***
</pre>
{% endraw %}
