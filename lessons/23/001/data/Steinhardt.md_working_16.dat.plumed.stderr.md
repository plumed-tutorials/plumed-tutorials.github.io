Stderr for source:  Steinhardt.md_working_16.dat   
Download: [zipped raw stdout](Steinhardt.md_working_16.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_16.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35749] *** Process received signal ***
[pkrvmbietmlfzoi:35749] Signal: Aborted (6)
[pkrvmbietmlfzoi:35749] Signal code:  (-6)
[pkrvmbietmlfzoi:35749] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f51a4845330]
[pkrvmbietmlfzoi:35749] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f51a489eb2c]
[pkrvmbietmlfzoi:35749] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f51a484527e]
[pkrvmbietmlfzoi:35749] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f51a48288ff]
[pkrvmbietmlfzoi:35749] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f51a4ca5ff5]
[pkrvmbietmlfzoi:35749] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f51a4cbb0da]
[pkrvmbietmlfzoi:35749] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f51a4ca5a55]
[pkrvmbietmlfzoi:35749] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f51a4ca5a6f]
[pkrvmbietmlfzoi:35749] [ 8] plumed(+0x13209)[0x55c8e63d5209]
[pkrvmbietmlfzoi:35749] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f51a482a1ca]
[pkrvmbietmlfzoi:35749] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f51a482a28b]
[pkrvmbietmlfzoi:35749] [11] plumed(+0x134a5)[0x55c8e63d54a5]
[pkrvmbietmlfzoi:35749] *** End of error message ***
</pre>
{% endraw %}
