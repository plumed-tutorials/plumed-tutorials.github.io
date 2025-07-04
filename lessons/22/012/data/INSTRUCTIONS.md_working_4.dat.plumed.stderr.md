Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:36278] *** Process received signal ***
[pkrvmbietmlfzoi:36278] Signal: Aborted (6)
[pkrvmbietmlfzoi:36278] Signal code:  (-6)
[pkrvmbietmlfzoi:36278] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f45a9c45330]
[pkrvmbietmlfzoi:36278] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f45a9c9eb2c]
[pkrvmbietmlfzoi:36278] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f45a9c4527e]
[pkrvmbietmlfzoi:36278] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f45a9c288ff]
[pkrvmbietmlfzoi:36278] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f45aa0a5ff5]
[pkrvmbietmlfzoi:36278] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f45aa0bb0da]
[pkrvmbietmlfzoi:36278] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f45aa0a5a55]
[pkrvmbietmlfzoi:36278] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f45aa0a5a6f]
[pkrvmbietmlfzoi:36278] [ 8] plumed(+0x13209)[0x5559ca1d0209]
[pkrvmbietmlfzoi:36278] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f45a9c2a1ca]
[pkrvmbietmlfzoi:36278] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f45a9c2a28b]
[pkrvmbietmlfzoi:36278] [11] plumed(+0x134a5)[0x5559ca1d04a5]
[pkrvmbietmlfzoi:36278] *** End of error message ***
</pre>
{% endraw %}
