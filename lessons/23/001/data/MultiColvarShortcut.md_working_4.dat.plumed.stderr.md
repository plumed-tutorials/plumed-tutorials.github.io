Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmbietmlfzoi:34850] *** Process received signal ***
[pkrvmbietmlfzoi:34850] Signal: Aborted (6)
[pkrvmbietmlfzoi:34850] Signal code:  (-6)
[pkrvmbietmlfzoi:34850] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb121a45330]
[pkrvmbietmlfzoi:34850] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb121a9eb2c]
[pkrvmbietmlfzoi:34850] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb121a4527e]
[pkrvmbietmlfzoi:34850] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb121a288ff]
[pkrvmbietmlfzoi:34850] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb121ea5ff5]
[pkrvmbietmlfzoi:34850] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb121ebb0da]
[pkrvmbietmlfzoi:34850] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb121ea5a55]
[pkrvmbietmlfzoi:34850] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb121ea5a6f]
[pkrvmbietmlfzoi:34850] [ 8] plumed(+0x13209)[0x557e7c45d209]
[pkrvmbietmlfzoi:34850] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb121a2a1ca]
[pkrvmbietmlfzoi:34850] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb121a2a28b]
[pkrvmbietmlfzoi:34850] [11] plumed(+0x134a5)[0x557e7c45d4a5]
[pkrvmbietmlfzoi:34850] *** End of error message ***
</pre>
{% endraw %}
