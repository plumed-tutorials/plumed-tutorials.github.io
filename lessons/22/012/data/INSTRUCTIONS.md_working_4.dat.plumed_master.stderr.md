Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmbietmlfzoi:36293] *** Process received signal ***
[pkrvmbietmlfzoi:36293] Signal: Aborted (6)
[pkrvmbietmlfzoi:36293] Signal code:  (-6)
[pkrvmbietmlfzoi:36293] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbc81645330]
[pkrvmbietmlfzoi:36293] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbc8169eb2c]
[pkrvmbietmlfzoi:36293] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbc8164527e]
[pkrvmbietmlfzoi:36293] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbc816288ff]
[pkrvmbietmlfzoi:36293] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbc81aa5ff5]
[pkrvmbietmlfzoi:36293] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbc81abb0da]
[pkrvmbietmlfzoi:36293] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbc81aa5a55]
[pkrvmbietmlfzoi:36293] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbc81aa5a6f]
[pkrvmbietmlfzoi:36293] [ 8] plumed_master(+0x146dd)[0x559c5b5a76dd]
[pkrvmbietmlfzoi:36293] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbc8162a1ca]
[pkrvmbietmlfzoi:36293] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbc8162a28b]
[pkrvmbietmlfzoi:36293] [11] plumed_master(+0x15365)[0x559c5b5a8365]
[pkrvmbietmlfzoi:36293] *** End of error message ***
</pre>
{% endraw %}
