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
[fv-az1279-640:06219] *** Process received signal ***
[fv-az1279-640:06219] Signal: Aborted (6)
[fv-az1279-640:06219] Signal code:  (-6)
[fv-az1279-640:06219] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9a63245330]
[fv-az1279-640:06219] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9a6329eb2c]
[fv-az1279-640:06219] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9a6324527e]
[fv-az1279-640:06219] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9a632288ff]
[fv-az1279-640:06219] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9a636a5ff5]
[fv-az1279-640:06219] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9a636bb0da]
[fv-az1279-640:06219] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9a636a5a55]
[fv-az1279-640:06219] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9a636a5a6f]
[fv-az1279-640:06219] [ 8] plumed(+0x13209)[0x558da71cd209]
[fv-az1279-640:06219] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9a6322a1ca]
[fv-az1279-640:06219] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9a6322a28b]
[fv-az1279-640:06219] [11] plumed(+0x134a5)[0x558da71cd4a5]
[fv-az1279-640:06219] *** End of error message ***
</pre>
{% endraw %}
