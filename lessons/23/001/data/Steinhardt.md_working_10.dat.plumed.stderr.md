Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[pkrvmbietmlfzoi:35555] *** Process received signal ***
[pkrvmbietmlfzoi:35555] Signal: Aborted (6)
[pkrvmbietmlfzoi:35555] Signal code:  (-6)
[pkrvmbietmlfzoi:35555] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4d4ac45330]
[pkrvmbietmlfzoi:35555] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4d4ac9eb2c]
[pkrvmbietmlfzoi:35555] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4d4ac4527e]
[pkrvmbietmlfzoi:35555] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4d4ac288ff]
[pkrvmbietmlfzoi:35555] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4d4b0a5ff5]
[pkrvmbietmlfzoi:35555] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4d4b0bb0da]
[pkrvmbietmlfzoi:35555] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4d4b0a5a55]
[pkrvmbietmlfzoi:35555] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4d4b0a5a6f]
[pkrvmbietmlfzoi:35555] [ 8] plumed(+0x13209)[0x557a6faeb209]
[pkrvmbietmlfzoi:35555] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4d4ac2a1ca]
[pkrvmbietmlfzoi:35555] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4d4ac2a28b]
[pkrvmbietmlfzoi:35555] [11] plumed(+0x134a5)[0x557a6faeb4a5]
[pkrvmbietmlfzoi:35555] *** End of error message ***
</pre>
{% endraw %}
