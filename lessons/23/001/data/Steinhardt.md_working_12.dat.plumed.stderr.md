Stderr for source:  Steinhardt.md_working_12.dat   
Download: [zipped raw stdout](Steinhardt.md_working_12.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_12.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35620] *** Process received signal ***
[pkrvmbietmlfzoi:35620] Signal: Aborted (6)
[pkrvmbietmlfzoi:35620] Signal code:  (-6)
[pkrvmbietmlfzoi:35620] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0385645330]
[pkrvmbietmlfzoi:35620] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f038569eb2c]
[pkrvmbietmlfzoi:35620] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f038564527e]
[pkrvmbietmlfzoi:35620] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f03856288ff]
[pkrvmbietmlfzoi:35620] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0385aa5ff5]
[pkrvmbietmlfzoi:35620] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0385abb0da]
[pkrvmbietmlfzoi:35620] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0385aa5a55]
[pkrvmbietmlfzoi:35620] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0385aa5a6f]
[pkrvmbietmlfzoi:35620] [ 8] plumed(+0x13209)[0x5625ebda7209]
[pkrvmbietmlfzoi:35620] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f038562a1ca]
[pkrvmbietmlfzoi:35620] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f038562a28b]
[pkrvmbietmlfzoi:35620] [11] plumed(+0x134a5)[0x5625ebda74a5]
[pkrvmbietmlfzoi:35620] *** End of error message ***
</pre>
{% endraw %}
