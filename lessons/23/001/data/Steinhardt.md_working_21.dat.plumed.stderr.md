Stderr for source:  Steinhardt.md_working_21.dat   
Download: [zipped raw stdout](Steinhardt.md_working_21.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_21.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35904] *** Process received signal ***
[pkrvmbietmlfzoi:35904] Signal: Aborted (6)
[pkrvmbietmlfzoi:35904] Signal code:  (-6)
[pkrvmbietmlfzoi:35904] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7148045330]
[pkrvmbietmlfzoi:35904] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f714809eb2c]
[pkrvmbietmlfzoi:35904] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f714804527e]
[pkrvmbietmlfzoi:35904] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f71480288ff]
[pkrvmbietmlfzoi:35904] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f71484a5ff5]
[pkrvmbietmlfzoi:35904] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f71484bb0da]
[pkrvmbietmlfzoi:35904] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f71484a5a55]
[pkrvmbietmlfzoi:35904] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f71484a5a6f]
[pkrvmbietmlfzoi:35904] [ 8] plumed(+0x13209)[0x55f899bb7209]
[pkrvmbietmlfzoi:35904] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f714802a1ca]
[pkrvmbietmlfzoi:35904] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f714802a28b]
[pkrvmbietmlfzoi:35904] [11] plumed(+0x134a5)[0x55f899bb74a5]
[pkrvmbietmlfzoi:35904] *** End of error message ***
</pre>
{% endraw %}
