Stderr for source:  Steinhardt.md_working_8.dat   
Download: [zipped raw stdout](Steinhardt.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35489] *** Process received signal ***
[pkrvmbietmlfzoi:35489] Signal: Aborted (6)
[pkrvmbietmlfzoi:35489] Signal code:  (-6)
[pkrvmbietmlfzoi:35489] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3dc2a45330]
[pkrvmbietmlfzoi:35489] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3dc2a9eb2c]
[pkrvmbietmlfzoi:35489] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3dc2a4527e]
[pkrvmbietmlfzoi:35489] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3dc2a288ff]
[pkrvmbietmlfzoi:35489] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3dc2ea5ff5]
[pkrvmbietmlfzoi:35489] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3dc2ebb0da]
[pkrvmbietmlfzoi:35489] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3dc2ea5a55]
[pkrvmbietmlfzoi:35489] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3dc2ea5a6f]
[pkrvmbietmlfzoi:35489] [ 8] plumed(+0x13209)[0x55a0cc9fc209]
[pkrvmbietmlfzoi:35489] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3dc2a2a1ca]
[pkrvmbietmlfzoi:35489] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3dc2a2a28b]
[pkrvmbietmlfzoi:35489] [11] plumed(+0x134a5)[0x55a0cc9fc4a5]
[pkrvmbietmlfzoi:35489] *** End of error message ***
</pre>
{% endraw %}
