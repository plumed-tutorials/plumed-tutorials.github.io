Stderr for source:  Steinhardt.md_working_5.dat   
Download: [zipped raw stdout](Steinhardt.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @1 : action q4 has no component named q4 (hint! the components in this actions are: )
[pkrvmbietmlfzoi:35396] *** Process received signal ***
[pkrvmbietmlfzoi:35396] Signal: Aborted (6)
[pkrvmbietmlfzoi:35396] Signal code:  (-6)
[pkrvmbietmlfzoi:35396] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3346c45330]
[pkrvmbietmlfzoi:35396] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3346c9eb2c]
[pkrvmbietmlfzoi:35396] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3346c4527e]
[pkrvmbietmlfzoi:35396] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3346c288ff]
[pkrvmbietmlfzoi:35396] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f33470a5ff5]
[pkrvmbietmlfzoi:35396] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f33470bb0da]
[pkrvmbietmlfzoi:35396] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f33470a5a55]
[pkrvmbietmlfzoi:35396] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f33470a5a6f]
[pkrvmbietmlfzoi:35396] [ 8] plumed(+0x13209)[0x55f3454b2209]
[pkrvmbietmlfzoi:35396] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3346c2a1ca]
[pkrvmbietmlfzoi:35396] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3346c2a28b]
[pkrvmbietmlfzoi:35396] [11] plumed(+0x134a5)[0x55f3454b24a5]
[pkrvmbietmlfzoi:35396] *** End of error message ***
</pre>
{% endraw %}
