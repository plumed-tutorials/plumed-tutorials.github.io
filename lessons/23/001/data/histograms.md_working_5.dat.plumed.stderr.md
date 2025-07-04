Stderr for source:  histograms.md_working_5.dat   
Download: [zipped raw stdout](histograms.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmbietmlfzoi:36819] *** Process received signal ***
[pkrvmbietmlfzoi:36819] Signal: Aborted (6)
[pkrvmbietmlfzoi:36819] Signal code:  (-6)
[pkrvmbietmlfzoi:36819] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f310c845330]
[pkrvmbietmlfzoi:36819] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f310c89eb2c]
[pkrvmbietmlfzoi:36819] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f310c84527e]
[pkrvmbietmlfzoi:36819] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f310c8288ff]
[pkrvmbietmlfzoi:36819] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f310cca5ff5]
[pkrvmbietmlfzoi:36819] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f310ccbb0da]
[pkrvmbietmlfzoi:36819] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f310cca5a55]
[pkrvmbietmlfzoi:36819] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f310cca5a6f]
[pkrvmbietmlfzoi:36819] [ 8] plumed(+0x13209)[0x557a7e323209]
[pkrvmbietmlfzoi:36819] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f310c82a1ca]
[pkrvmbietmlfzoi:36819] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f310c82a28b]
[pkrvmbietmlfzoi:36819] [11] plumed(+0x134a5)[0x557a7e3234a5]
[pkrvmbietmlfzoi:36819] *** End of error message ***
</pre>
{% endraw %}
