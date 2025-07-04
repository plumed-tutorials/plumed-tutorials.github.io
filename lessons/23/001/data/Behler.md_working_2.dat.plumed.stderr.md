Stderr for source:  Behler.md_working_2.dat   
Download: [zipped raw stdout](Behler.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:36004] *** Process received signal ***
[pkrvmbietmlfzoi:36004] Signal: Aborted (6)
[pkrvmbietmlfzoi:36004] Signal code:  (-6)
[pkrvmbietmlfzoi:36004] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f54cba45330]
[pkrvmbietmlfzoi:36004] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f54cba9eb2c]
[pkrvmbietmlfzoi:36004] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f54cba4527e]
[pkrvmbietmlfzoi:36004] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f54cba288ff]
[pkrvmbietmlfzoi:36004] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f54cbea5ff5]
[pkrvmbietmlfzoi:36004] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f54cbebb0da]
[pkrvmbietmlfzoi:36004] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f54cbea5a55]
[pkrvmbietmlfzoi:36004] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f54cbea5a6f]
[pkrvmbietmlfzoi:36004] [ 8] plumed(+0x13209)[0x564fc62c3209]
[pkrvmbietmlfzoi:36004] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f54cba2a1ca]
[pkrvmbietmlfzoi:36004] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f54cba2a28b]
[pkrvmbietmlfzoi:36004] [11] plumed(+0x134a5)[0x564fc62c34a5]
[pkrvmbietmlfzoi:36004] *** End of error message ***
</pre>
{% endraw %}
