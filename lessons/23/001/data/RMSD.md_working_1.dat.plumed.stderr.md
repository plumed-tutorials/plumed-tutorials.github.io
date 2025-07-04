Stderr for source:  RMSD.md_working_1.dat   
Download: [zipped raw stdout](RMSD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONSTANT with label v : cannot understand the following words from the input line : NCOLS=12, NROWS=2
[pkrvmbietmlfzoi:37241] *** Process received signal ***
[pkrvmbietmlfzoi:37241] Signal: Aborted (6)
[pkrvmbietmlfzoi:37241] Signal code:  (-6)
[pkrvmbietmlfzoi:37241] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3a56e45330]
[pkrvmbietmlfzoi:37241] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3a56e9eb2c]
[pkrvmbietmlfzoi:37241] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3a56e4527e]
[pkrvmbietmlfzoi:37241] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3a56e288ff]
[pkrvmbietmlfzoi:37241] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3a572a5ff5]
[pkrvmbietmlfzoi:37241] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3a572bb0da]
[pkrvmbietmlfzoi:37241] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3a572a5a55]
[pkrvmbietmlfzoi:37241] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3a572a5a6f]
[pkrvmbietmlfzoi:37241] [ 8] plumed(+0x13209)[0x5610ed3ef209]
[pkrvmbietmlfzoi:37241] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3a56e2a1ca]
[pkrvmbietmlfzoi:37241] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3a56e2a28b]
[pkrvmbietmlfzoi:37241] [11] plumed(+0x134a5)[0x5610ed3ef4a5]
[pkrvmbietmlfzoi:37241] *** End of error message ***
</pre>
{% endraw %}
