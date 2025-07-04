Stderr for source:  RMSD.md_working_6.dat   
Download: [zipped raw stdout](RMSD.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action RMSD with label rmsd : cannot understand the following words from the input line : DISPLACEMENT
[pkrvmbietmlfzoi:37385] *** Process received signal ***
[pkrvmbietmlfzoi:37385] Signal: Aborted (6)
[pkrvmbietmlfzoi:37385] Signal code:  (-6)
[pkrvmbietmlfzoi:37385] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f10b9845330]
[pkrvmbietmlfzoi:37385] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f10b989eb2c]
[pkrvmbietmlfzoi:37385] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f10b984527e]
[pkrvmbietmlfzoi:37385] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f10b98288ff]
[pkrvmbietmlfzoi:37385] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f10b9ca5ff5]
[pkrvmbietmlfzoi:37385] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f10b9cbb0da]
[pkrvmbietmlfzoi:37385] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f10b9ca5a55]
[pkrvmbietmlfzoi:37385] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f10b9ca5a6f]
[pkrvmbietmlfzoi:37385] [ 8] plumed(+0x13209)[0x556b73c1a209]
[pkrvmbietmlfzoi:37385] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f10b982a1ca]
[pkrvmbietmlfzoi:37385] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f10b982a28b]
[pkrvmbietmlfzoi:37385] [11] plumed(+0x134a5)[0x556b73c1a4a5]
[pkrvmbietmlfzoi:37385] *** End of error message ***
</pre>
{% endraw %}
