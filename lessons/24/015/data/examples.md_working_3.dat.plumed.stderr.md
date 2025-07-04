Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35333] *** Process received signal ***
[pkrvmbietmlfzoi:35333] Signal: Aborted (6)
[pkrvmbietmlfzoi:35333] Signal code:  (-6)
[pkrvmbietmlfzoi:35333] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8907445330]
[pkrvmbietmlfzoi:35333] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f890749eb2c]
[pkrvmbietmlfzoi:35333] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f890744527e]
[pkrvmbietmlfzoi:35333] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f89074288ff]
[pkrvmbietmlfzoi:35333] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f89078a5ff5]
[pkrvmbietmlfzoi:35333] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f89078bb0da]
[pkrvmbietmlfzoi:35333] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f89078a5a55]
[pkrvmbietmlfzoi:35333] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f89078a5a6f]
[pkrvmbietmlfzoi:35333] [ 8] plumed(+0x13209)[0x55745928b209]
[pkrvmbietmlfzoi:35333] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f890742a1ca]
[pkrvmbietmlfzoi:35333] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f890742a28b]
[pkrvmbietmlfzoi:35333] [11] plumed(+0x134a5)[0x55745928b4a5]
[pkrvmbietmlfzoi:35333] *** End of error message ***
</pre>
{% endraw %}
