Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label uwall : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:36366] *** Process received signal ***
[pkrvmbietmlfzoi:36366] Signal: Aborted (6)
[pkrvmbietmlfzoi:36366] Signal code:  (-6)
[pkrvmbietmlfzoi:36366] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8310c45330]
[pkrvmbietmlfzoi:36366] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8310c9eb2c]
[pkrvmbietmlfzoi:36366] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8310c4527e]
[pkrvmbietmlfzoi:36366] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8310c288ff]
[pkrvmbietmlfzoi:36366] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f83110a5ff5]
[pkrvmbietmlfzoi:36366] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f83110bb0da]
[pkrvmbietmlfzoi:36366] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f83110a5a55]
[pkrvmbietmlfzoi:36366] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f83110a5a6f]
[pkrvmbietmlfzoi:36366] [ 8] plumed(+0x13209)[0x555ec4425209]
[pkrvmbietmlfzoi:36366] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8310c2a1ca]
[pkrvmbietmlfzoi:36366] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8310c2a28b]
[pkrvmbietmlfzoi:36366] [11] plumed(+0x134a5)[0x555ec44254a5]
[pkrvmbietmlfzoi:36366] *** End of error message ***
</pre>
{% endraw %}
