Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmbietmlfzoi:35286] *** Process received signal ***
[pkrvmbietmlfzoi:35286] Signal: Aborted (6)
[pkrvmbietmlfzoi:35286] Signal code:  (-6)
[pkrvmbietmlfzoi:35286] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4446045330]
[pkrvmbietmlfzoi:35286] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f444609eb2c]
[pkrvmbietmlfzoi:35286] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f444604527e]
[pkrvmbietmlfzoi:35286] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f44460288ff]
[pkrvmbietmlfzoi:35286] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f44464a5ff5]
[pkrvmbietmlfzoi:35286] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f44464bb0da]
[pkrvmbietmlfzoi:35286] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f44464a5a55]
[pkrvmbietmlfzoi:35286] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f44464a5a6f]
[pkrvmbietmlfzoi:35286] [ 8] plumed_master(+0x146dd)[0x5598310f16dd]
[pkrvmbietmlfzoi:35286] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f444602a1ca]
[pkrvmbietmlfzoi:35286] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f444602a28b]
[pkrvmbietmlfzoi:35286] [11] plumed_master(+0x15365)[0x5598310f2365]
[pkrvmbietmlfzoi:35286] *** End of error message ***
</pre>
{% endraw %}
