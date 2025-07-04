Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmbietmlfzoi:35331] *** Process received signal ***
[pkrvmbietmlfzoi:35331] Signal: Aborted (6)
[pkrvmbietmlfzoi:35331] Signal code:  (-6)
[pkrvmbietmlfzoi:35331] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f841dc45330]
[pkrvmbietmlfzoi:35331] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f841dc9eb2c]
[pkrvmbietmlfzoi:35331] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f841dc4527e]
[pkrvmbietmlfzoi:35331] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f841dc288ff]
[pkrvmbietmlfzoi:35331] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f841e0a5ff5]
[pkrvmbietmlfzoi:35331] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f841e0bb0da]
[pkrvmbietmlfzoi:35331] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f841e0a5a55]
[pkrvmbietmlfzoi:35331] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f841e0a5a6f]
[pkrvmbietmlfzoi:35331] [ 8] plumed_master(+0x146dd)[0x561e106b26dd]
[pkrvmbietmlfzoi:35331] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f841dc2a1ca]
[pkrvmbietmlfzoi:35331] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f841dc2a28b]
[pkrvmbietmlfzoi:35331] [11] plumed_master(+0x15365)[0x561e106b3365]
[pkrvmbietmlfzoi:35331] *** End of error message ***
</pre>
{% endraw %}
