Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(vesselbase/Vessel.cpp:157) void PLMD::vesselbase::Vessel::error(const std::string&)
ERROR for keyword MORE_THAN in action CLUSTER_DISTRIBUTION with label nclust : could not parse D_0
[pkrvmbietmlfzoi:35532] *** Process received signal ***
[pkrvmbietmlfzoi:35532] Signal: Aborted (6)
[pkrvmbietmlfzoi:35532] Signal code:  (-6)
[pkrvmbietmlfzoi:35532] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8527845330]
[pkrvmbietmlfzoi:35532] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f852789eb2c]
[pkrvmbietmlfzoi:35532] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f852784527e]
[pkrvmbietmlfzoi:35532] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f85278288ff]
[pkrvmbietmlfzoi:35532] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8527ca5ff5]
[pkrvmbietmlfzoi:35532] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8527cbb0da]
[pkrvmbietmlfzoi:35532] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8527ca5a55]
[pkrvmbietmlfzoi:35532] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8527ca5a6f]
[pkrvmbietmlfzoi:35532] [ 8] plumed(+0x13209)[0x55cc217c4209]
[pkrvmbietmlfzoi:35532] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f852782a1ca]
[pkrvmbietmlfzoi:35532] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f852782a28b]
[pkrvmbietmlfzoi:35532] [11] plumed(+0x134a5)[0x55cc217c44a5]
[pkrvmbietmlfzoi:35532] *** End of error message ***
</pre>
{% endraw %}
