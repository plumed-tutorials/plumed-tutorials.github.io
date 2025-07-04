Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[pkrvmbietmlfzoi:36322] *** Process received signal ***
[pkrvmbietmlfzoi:36322] Signal: Aborted (6)
[pkrvmbietmlfzoi:36322] Signal code:  (-6)
[pkrvmbietmlfzoi:36322] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f59c1045330]
[pkrvmbietmlfzoi:36322] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f59c109eb2c]
[pkrvmbietmlfzoi:36322] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f59c104527e]
[pkrvmbietmlfzoi:36322] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f59c10288ff]
[pkrvmbietmlfzoi:36322] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f59c14a5ff5]
[pkrvmbietmlfzoi:36322] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f59c14bb0da]
[pkrvmbietmlfzoi:36322] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f59c14a5a55]
[pkrvmbietmlfzoi:36322] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f59c14a5a6f]
[pkrvmbietmlfzoi:36322] [ 8] plumed(+0x13209)[0x5631e7304209]
[pkrvmbietmlfzoi:36322] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f59c102a1ca]
[pkrvmbietmlfzoi:36322] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f59c102a28b]
[pkrvmbietmlfzoi:36322] [11] plumed(+0x134a5)[0x5631e73044a5]
[pkrvmbietmlfzoi:36322] *** End of error message ***
</pre>
{% endraw %}
