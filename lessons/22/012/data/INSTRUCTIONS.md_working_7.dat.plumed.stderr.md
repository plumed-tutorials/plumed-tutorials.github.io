Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:36411] *** Process received signal ***
[pkrvmbietmlfzoi:36411] Signal: Aborted (6)
[pkrvmbietmlfzoi:36411] Signal code:  (-6)
[pkrvmbietmlfzoi:36411] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe2f8045330]
[pkrvmbietmlfzoi:36411] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe2f809eb2c]
[pkrvmbietmlfzoi:36411] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe2f804527e]
[pkrvmbietmlfzoi:36411] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe2f80288ff]
[pkrvmbietmlfzoi:36411] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe2f84a5ff5]
[pkrvmbietmlfzoi:36411] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe2f84bb0da]
[pkrvmbietmlfzoi:36411] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe2f84a5a55]
[pkrvmbietmlfzoi:36411] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe2f84a5a6f]
[pkrvmbietmlfzoi:36411] [ 8] plumed(+0x13209)[0x560ff9dd2209]
[pkrvmbietmlfzoi:36411] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe2f802a1ca]
[pkrvmbietmlfzoi:36411] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe2f802a28b]
[pkrvmbietmlfzoi:36411] [11] plumed(+0x134a5)[0x560ff9dd24a5]
[pkrvmbietmlfzoi:36411] *** End of error message ***
</pre>
{% endraw %}
