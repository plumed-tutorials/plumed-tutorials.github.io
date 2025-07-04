Stderr for source:  Steinhardt.md_working_6.dat   
Download: [zipped raw stdout](Steinhardt.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35427] *** Process received signal ***
[pkrvmbietmlfzoi:35427] Signal: Aborted (6)
[pkrvmbietmlfzoi:35427] Signal code:  (-6)
[pkrvmbietmlfzoi:35427] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f43e3845330]
[pkrvmbietmlfzoi:35427] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f43e389eb2c]
[pkrvmbietmlfzoi:35427] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f43e384527e]
[pkrvmbietmlfzoi:35427] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f43e38288ff]
[pkrvmbietmlfzoi:35427] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f43e3ca5ff5]
[pkrvmbietmlfzoi:35427] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f43e3cbb0da]
[pkrvmbietmlfzoi:35427] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f43e3ca5a55]
[pkrvmbietmlfzoi:35427] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f43e3ca5a6f]
[pkrvmbietmlfzoi:35427] [ 8] plumed(+0x13209)[0x557c3661d209]
[pkrvmbietmlfzoi:35427] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f43e382a1ca]
[pkrvmbietmlfzoi:35427] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f43e382a28b]
[pkrvmbietmlfzoi:35427] [11] plumed(+0x134a5)[0x557c3661d4a5]
[pkrvmbietmlfzoi:35427] *** End of error message ***
</pre>
{% endraw %}
