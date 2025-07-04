Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:34934] *** Process received signal ***
[pkrvmbietmlfzoi:34934] Signal: Aborted (6)
[pkrvmbietmlfzoi:34934] Signal code:  (-6)
[pkrvmbietmlfzoi:34934] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0d85c45330]
[pkrvmbietmlfzoi:34934] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0d85c9eb2c]
[pkrvmbietmlfzoi:34934] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0d85c4527e]
[pkrvmbietmlfzoi:34934] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0d85c288ff]
[pkrvmbietmlfzoi:34934] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0d860a5ff5]
[pkrvmbietmlfzoi:34934] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0d860bb0da]
[pkrvmbietmlfzoi:34934] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0d860a5a55]
[pkrvmbietmlfzoi:34934] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0d860a5a6f]
[pkrvmbietmlfzoi:34934] [ 8] plumed(+0x13209)[0x559605953209]
[pkrvmbietmlfzoi:34934] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0d85c2a1ca]
[pkrvmbietmlfzoi:34934] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0d85c2a28b]
[pkrvmbietmlfzoi:34934] [11] plumed(+0x134a5)[0x5596059534a5]
[pkrvmbietmlfzoi:34934] *** End of error message ***
</pre>
{% endraw %}
