Stderr for source:  SymmetryFunction.md_working_3.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[pkrvmbietmlfzoi:36343] *** Process received signal ***
[pkrvmbietmlfzoi:36343] Signal: Aborted (6)
[pkrvmbietmlfzoi:36343] Signal code:  (-6)
[pkrvmbietmlfzoi:36343] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f559be45330]
[pkrvmbietmlfzoi:36343] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f559be9eb2c]
[pkrvmbietmlfzoi:36343] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f559be4527e]
[pkrvmbietmlfzoi:36343] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f559be288ff]
[pkrvmbietmlfzoi:36343] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f559c2a5ff5]
[pkrvmbietmlfzoi:36343] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f559c2bb0da]
[pkrvmbietmlfzoi:36343] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f559c2a5a55]
[pkrvmbietmlfzoi:36343] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f559c2a5a6f]
[pkrvmbietmlfzoi:36343] [ 8] plumed(+0x13209)[0x561f458ee209]
[pkrvmbietmlfzoi:36343] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f559be2a1ca]
[pkrvmbietmlfzoi:36343] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f559be2a28b]
[pkrvmbietmlfzoi:36343] [11] plumed(+0x134a5)[0x561f458ee4a5]
[pkrvmbietmlfzoi:36343] *** End of error message ***
</pre>
{% endraw %}
