Stderr for source:  SymmetryFunction.md_working_2.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[pkrvmbietmlfzoi:36312] *** Process received signal ***
[pkrvmbietmlfzoi:36312] Signal: Aborted (6)
[pkrvmbietmlfzoi:36312] Signal code:  (-6)
[pkrvmbietmlfzoi:36312] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f30d8c45330]
[pkrvmbietmlfzoi:36312] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f30d8c9eb2c]
[pkrvmbietmlfzoi:36312] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f30d8c4527e]
[pkrvmbietmlfzoi:36312] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f30d8c288ff]
[pkrvmbietmlfzoi:36312] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f30d90a5ff5]
[pkrvmbietmlfzoi:36312] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f30d90bb0da]
[pkrvmbietmlfzoi:36312] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f30d90a5a55]
[pkrvmbietmlfzoi:36312] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f30d90a5a6f]
[pkrvmbietmlfzoi:36312] [ 8] plumed(+0x13209)[0x56521083b209]
[pkrvmbietmlfzoi:36312] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f30d8c2a1ca]
[pkrvmbietmlfzoi:36312] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f30d8c2a28b]
[pkrvmbietmlfzoi:36312] [11] plumed(+0x134a5)[0x56521083b4a5]
[pkrvmbietmlfzoi:36312] *** End of error message ***
</pre>
{% endraw %}
