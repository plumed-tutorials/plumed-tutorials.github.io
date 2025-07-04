Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmbietmlfzoi:36427] *** Process received signal ***
[pkrvmbietmlfzoi:36427] Signal: Aborted (6)
[pkrvmbietmlfzoi:36427] Signal code:  (-6)
[pkrvmbietmlfzoi:36427] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9c07445330]
[pkrvmbietmlfzoi:36427] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9c0749eb2c]
[pkrvmbietmlfzoi:36427] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9c0744527e]
[pkrvmbietmlfzoi:36427] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9c074288ff]
[pkrvmbietmlfzoi:36427] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9c078a5ff5]
[pkrvmbietmlfzoi:36427] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9c078bb0da]
[pkrvmbietmlfzoi:36427] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9c078a5a55]
[pkrvmbietmlfzoi:36427] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9c078a5a6f]
[pkrvmbietmlfzoi:36427] [ 8] plumed_master(+0x146dd)[0x55dd835326dd]
[pkrvmbietmlfzoi:36427] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9c0742a1ca]
[pkrvmbietmlfzoi:36427] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9c0742a28b]
[pkrvmbietmlfzoi:36427] [11] plumed_master(+0x15365)[0x55dd83533365]
[pkrvmbietmlfzoi:36427] *** End of error message ***
</pre>
{% endraw %}
