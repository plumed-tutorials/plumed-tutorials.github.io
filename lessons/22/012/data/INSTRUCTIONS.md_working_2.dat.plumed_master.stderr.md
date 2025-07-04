Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label @s9 : keyword SIGMA could not be read correctly
[pkrvmbietmlfzoi:36232] *** Process received signal ***
[pkrvmbietmlfzoi:36232] Signal: Aborted (6)
[pkrvmbietmlfzoi:36232] Signal code:  (-6)
[pkrvmbietmlfzoi:36232] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffa86445330]
[pkrvmbietmlfzoi:36232] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffa8649eb2c]
[pkrvmbietmlfzoi:36232] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffa8644527e]
[pkrvmbietmlfzoi:36232] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffa864288ff]
[pkrvmbietmlfzoi:36232] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffa868a5ff5]
[pkrvmbietmlfzoi:36232] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffa868bb0da]
[pkrvmbietmlfzoi:36232] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffa868a5a55]
[pkrvmbietmlfzoi:36232] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffa868a5a6f]
[pkrvmbietmlfzoi:36232] [ 8] plumed_master(+0x146dd)[0x55ff7ce096dd]
[pkrvmbietmlfzoi:36232] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffa8642a1ca]
[pkrvmbietmlfzoi:36232] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffa8642a28b]
[pkrvmbietmlfzoi:36232] [11] plumed_master(+0x15365)[0x55ff7ce0a365]
[pkrvmbietmlfzoi:36232] *** End of error message ***
</pre>
{% endraw %}
