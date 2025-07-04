Stderr for source:  Volumes.md_working_1.dat   
Download: [zipped raw stdout](Volumes.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[pkrvmbietmlfzoi:36168] *** Process received signal ***
[pkrvmbietmlfzoi:36168] Signal: Aborted (6)
[pkrvmbietmlfzoi:36168] Signal code:  (-6)
[pkrvmbietmlfzoi:36168] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f47f4645330]
[pkrvmbietmlfzoi:36168] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f47f469eb2c]
[pkrvmbietmlfzoi:36168] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f47f464527e]
[pkrvmbietmlfzoi:36168] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f47f46288ff]
[pkrvmbietmlfzoi:36168] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f47f4aa5ff5]
[pkrvmbietmlfzoi:36168] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f47f4abb0da]
[pkrvmbietmlfzoi:36168] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f47f4aa5a55]
[pkrvmbietmlfzoi:36168] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f47f4aa5a6f]
[pkrvmbietmlfzoi:36168] [ 8] plumed(+0x13209)[0x55877d239209]
[pkrvmbietmlfzoi:36168] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f47f462a1ca]
[pkrvmbietmlfzoi:36168] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f47f462a28b]
[pkrvmbietmlfzoi:36168] [11] plumed(+0x134a5)[0x55877d2394a5]
[pkrvmbietmlfzoi:36168] *** End of error message ***
</pre>
{% endraw %}
