Stderr for source:  Sprint.md_working_1.dat   
Download: [zipped raw stdout](Sprint.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label s1 : keyword MATRIX is compulsory for this action
[pkrvmbietmlfzoi:35155] *** Process received signal ***
[pkrvmbietmlfzoi:35155] Signal: Aborted (6)
[pkrvmbietmlfzoi:35155] Signal code:  (-6)
[pkrvmbietmlfzoi:35155] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4394645330]
[pkrvmbietmlfzoi:35155] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f439469eb2c]
[pkrvmbietmlfzoi:35155] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f439464527e]
[pkrvmbietmlfzoi:35155] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f43946288ff]
[pkrvmbietmlfzoi:35155] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4394aa5ff5]
[pkrvmbietmlfzoi:35155] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4394abb0da]
[pkrvmbietmlfzoi:35155] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4394aa5a55]
[pkrvmbietmlfzoi:35155] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4394aa5a6f]
[pkrvmbietmlfzoi:35155] [ 8] plumed(+0x13209)[0x557bf348f209]
[pkrvmbietmlfzoi:35155] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f439462a1ca]
[pkrvmbietmlfzoi:35155] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f439462a28b]
[pkrvmbietmlfzoi:35155] [11] plumed(+0x134a5)[0x557bf348f4a5]
[pkrvmbietmlfzoi:35155] *** End of error message ***
</pre>
{% endraw %}
