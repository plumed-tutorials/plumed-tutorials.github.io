Stderr for source:  Volumes.md_working_3.dat   
Download: [zipped raw stdout](Volumes.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:36231] *** Process received signal ***
[pkrvmbietmlfzoi:36231] Signal: Aborted (6)
[pkrvmbietmlfzoi:36231] Signal code:  (-6)
[pkrvmbietmlfzoi:36231] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4370645330]
[pkrvmbietmlfzoi:36231] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f437069eb2c]
[pkrvmbietmlfzoi:36231] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f437064527e]
[pkrvmbietmlfzoi:36231] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f43706288ff]
[pkrvmbietmlfzoi:36231] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4370aa5ff5]
[pkrvmbietmlfzoi:36231] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4370abb0da]
[pkrvmbietmlfzoi:36231] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4370aa5a55]
[pkrvmbietmlfzoi:36231] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4370aa5a6f]
[pkrvmbietmlfzoi:36231] [ 8] plumed(+0x13209)[0x55a217663209]
[pkrvmbietmlfzoi:36231] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f437062a1ca]
[pkrvmbietmlfzoi:36231] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f437062a28b]
[pkrvmbietmlfzoi:36231] [11] plumed(+0x134a5)[0x55a2176634a5]
[pkrvmbietmlfzoi:36231] *** End of error message ***
</pre>
{% endraw %}
