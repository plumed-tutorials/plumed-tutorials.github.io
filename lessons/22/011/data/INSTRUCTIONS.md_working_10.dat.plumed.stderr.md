Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmbietmlfzoi:35315] *** Process received signal ***
[pkrvmbietmlfzoi:35315] Signal: Aborted (6)
[pkrvmbietmlfzoi:35315] Signal code:  (-6)
[pkrvmbietmlfzoi:35315] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff2d1445330]
[pkrvmbietmlfzoi:35315] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff2d149eb2c]
[pkrvmbietmlfzoi:35315] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff2d144527e]
[pkrvmbietmlfzoi:35315] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff2d14288ff]
[pkrvmbietmlfzoi:35315] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff2d18a5ff5]
[pkrvmbietmlfzoi:35315] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff2d18bb0da]
[pkrvmbietmlfzoi:35315] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff2d18a5a55]
[pkrvmbietmlfzoi:35315] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff2d18a5a6f]
[pkrvmbietmlfzoi:35315] [ 8] plumed(+0x13209)[0x564709400209]
[pkrvmbietmlfzoi:35315] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff2d142a1ca]
[pkrvmbietmlfzoi:35315] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff2d142a28b]
[pkrvmbietmlfzoi:35315] [11] plumed(+0x134a5)[0x5647094004a5]
[pkrvmbietmlfzoi:35315] *** End of error message ***
</pre>
{% endraw %}
