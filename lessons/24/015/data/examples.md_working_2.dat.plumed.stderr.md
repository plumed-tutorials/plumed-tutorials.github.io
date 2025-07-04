Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35287] *** Process received signal ***
[pkrvmbietmlfzoi:35287] Signal: Aborted (6)
[pkrvmbietmlfzoi:35287] Signal code:  (-6)
[pkrvmbietmlfzoi:35287] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f218d645330]
[pkrvmbietmlfzoi:35287] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f218d69eb2c]
[pkrvmbietmlfzoi:35287] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f218d64527e]
[pkrvmbietmlfzoi:35287] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f218d6288ff]
[pkrvmbietmlfzoi:35287] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f218daa5ff5]
[pkrvmbietmlfzoi:35287] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f218dabb0da]
[pkrvmbietmlfzoi:35287] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f218daa5a55]
[pkrvmbietmlfzoi:35287] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f218daa5a6f]
[pkrvmbietmlfzoi:35287] [ 8] plumed(+0x13209)[0x55d9b82f5209]
[pkrvmbietmlfzoi:35287] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f218d62a1ca]
[pkrvmbietmlfzoi:35287] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f218d62a28b]
[pkrvmbietmlfzoi:35287] [11] plumed(+0x134a5)[0x55d9b82f54a5]
[pkrvmbietmlfzoi:35287] *** End of error message ***
</pre>
{% endraw %}
