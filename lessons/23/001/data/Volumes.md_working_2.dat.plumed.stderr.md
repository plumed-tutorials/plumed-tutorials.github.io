Stderr for source:  Volumes.md_working_2.dat   
Download: [zipped raw stdout](Volumes.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[pkrvmbietmlfzoi:36200] *** Process received signal ***
[pkrvmbietmlfzoi:36200] Signal: Aborted (6)
[pkrvmbietmlfzoi:36200] Signal code:  (-6)
[pkrvmbietmlfzoi:36200] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5d75e45330]
[pkrvmbietmlfzoi:36200] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5d75e9eb2c]
[pkrvmbietmlfzoi:36200] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5d75e4527e]
[pkrvmbietmlfzoi:36200] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5d75e288ff]
[pkrvmbietmlfzoi:36200] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5d762a5ff5]
[pkrvmbietmlfzoi:36200] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5d762bb0da]
[pkrvmbietmlfzoi:36200] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5d762a5a55]
[pkrvmbietmlfzoi:36200] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5d762a5a6f]
[pkrvmbietmlfzoi:36200] [ 8] plumed(+0x13209)[0x5607eae37209]
[pkrvmbietmlfzoi:36200] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5d75e2a1ca]
[pkrvmbietmlfzoi:36200] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5d75e2a28b]
[pkrvmbietmlfzoi:36200] [11] plumed(+0x134a5)[0x5607eae374a5]
[pkrvmbietmlfzoi:36200] *** End of error message ***
</pre>
{% endraw %}
