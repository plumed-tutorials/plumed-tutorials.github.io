Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[pkrvmbietmlfzoi:35360] *** Process received signal ***
[pkrvmbietmlfzoi:35360] Signal: Aborted (6)
[pkrvmbietmlfzoi:35360] Signal code:  (-6)
[pkrvmbietmlfzoi:35360] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb14ec45330]
[pkrvmbietmlfzoi:35360] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb14ec9eb2c]
[pkrvmbietmlfzoi:35360] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb14ec4527e]
[pkrvmbietmlfzoi:35360] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb14ec288ff]
[pkrvmbietmlfzoi:35360] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb14f0a5ff5]
[pkrvmbietmlfzoi:35360] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb14f0bb0da]
[pkrvmbietmlfzoi:35360] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb14f0a5a55]
[pkrvmbietmlfzoi:35360] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb14f0a5a6f]
[pkrvmbietmlfzoi:35360] [ 8] plumed_master(+0x146dd)[0x55ddc5db96dd]
[pkrvmbietmlfzoi:35360] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb14ec2a1ca]
[pkrvmbietmlfzoi:35360] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb14ec2a28b]
[pkrvmbietmlfzoi:35360] [11] plumed_master(+0x15365)[0x55ddc5dba365]
[pkrvmbietmlfzoi:35360] *** End of error message ***
</pre>
{% endraw %}
