Stderr for source:  Clusters.md_working_2.dat   
Download: [zipped raw stdout](Clusters.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[pkrvmbietmlfzoi:37171] *** Process received signal ***
[pkrvmbietmlfzoi:37171] Signal: Aborted (6)
[pkrvmbietmlfzoi:37171] Signal code:  (-6)
[pkrvmbietmlfzoi:37171] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f573e245330]
[pkrvmbietmlfzoi:37171] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f573e29eb2c]
[pkrvmbietmlfzoi:37171] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f573e24527e]
[pkrvmbietmlfzoi:37171] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f573e2288ff]
[pkrvmbietmlfzoi:37171] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f573e6a5ff5]
[pkrvmbietmlfzoi:37171] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f573e6bb0da]
[pkrvmbietmlfzoi:37171] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f573e6a5a55]
[pkrvmbietmlfzoi:37171] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f573e6a5a6f]
[pkrvmbietmlfzoi:37171] [ 8] plumed(+0x13209)[0x55ec50d28209]
[pkrvmbietmlfzoi:37171] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f573e22a1ca]
[pkrvmbietmlfzoi:37171] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f573e22a28b]
[pkrvmbietmlfzoi:37171] [11] plumed(+0x134a5)[0x55ec50d284a5]
[pkrvmbietmlfzoi:37171] *** End of error message ***
</pre>
{% endraw %}
