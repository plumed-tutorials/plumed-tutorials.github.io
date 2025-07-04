Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[pkrvmbietmlfzoi:37203] *** Process received signal ***
[pkrvmbietmlfzoi:37203] Signal: Aborted (6)
[pkrvmbietmlfzoi:37203] Signal code:  (-6)
[pkrvmbietmlfzoi:37203] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f914b845330]
[pkrvmbietmlfzoi:37203] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f914b89eb2c]
[pkrvmbietmlfzoi:37203] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f914b84527e]
[pkrvmbietmlfzoi:37203] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f914b8288ff]
[pkrvmbietmlfzoi:37203] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f914bca5ff5]
[pkrvmbietmlfzoi:37203] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f914bcbb0da]
[pkrvmbietmlfzoi:37203] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f914bca5a55]
[pkrvmbietmlfzoi:37203] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f914bca5a6f]
[pkrvmbietmlfzoi:37203] [ 8] plumed(+0x13209)[0x564cc9496209]
[pkrvmbietmlfzoi:37203] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f914b82a1ca]
[pkrvmbietmlfzoi:37203] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f914b82a28b]
[pkrvmbietmlfzoi:37203] [11] plumed(+0x134a5)[0x564cc94964a5]
[pkrvmbietmlfzoi:37203] *** End of error message ***
</pre>
{% endraw %}
