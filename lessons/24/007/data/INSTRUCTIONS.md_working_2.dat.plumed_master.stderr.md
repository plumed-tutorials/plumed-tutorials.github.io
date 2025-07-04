Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[pkrvmbietmlfzoi:35315] *** Process received signal ***
[pkrvmbietmlfzoi:35315] Signal: Aborted (6)
[pkrvmbietmlfzoi:35315] Signal code:  (-6)
[pkrvmbietmlfzoi:35315] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb43c445330]
[pkrvmbietmlfzoi:35315] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb43c49eb2c]
[pkrvmbietmlfzoi:35315] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb43c44527e]
[pkrvmbietmlfzoi:35315] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb43c4288ff]
[pkrvmbietmlfzoi:35315] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb43c8a5ff5]
[pkrvmbietmlfzoi:35315] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb43c8bb0da]
[pkrvmbietmlfzoi:35315] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb43c8a5a55]
[pkrvmbietmlfzoi:35315] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb43c8a5a6f]
[pkrvmbietmlfzoi:35315] [ 8] plumed_master(+0x146dd)[0x557eb10136dd]
[pkrvmbietmlfzoi:35315] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb43c42a1ca]
[pkrvmbietmlfzoi:35315] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb43c42a28b]
[pkrvmbietmlfzoi:35315] [11] plumed_master(+0x15365)[0x557eb1014365]
[pkrvmbietmlfzoi:35315] *** End of error message ***
</pre>
{% endraw %}
