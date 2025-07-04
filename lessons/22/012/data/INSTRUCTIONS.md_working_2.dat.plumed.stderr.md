Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[pkrvmbietmlfzoi:36216] *** Process received signal ***
[pkrvmbietmlfzoi:36216] Signal: Aborted (6)
[pkrvmbietmlfzoi:36216] Signal code:  (-6)
[pkrvmbietmlfzoi:36216] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f92b2e45330]
[pkrvmbietmlfzoi:36216] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f92b2e9eb2c]
[pkrvmbietmlfzoi:36216] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f92b2e4527e]
[pkrvmbietmlfzoi:36216] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f92b2e288ff]
[pkrvmbietmlfzoi:36216] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f92b32a5ff5]
[pkrvmbietmlfzoi:36216] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f92b32bb0da]
[pkrvmbietmlfzoi:36216] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f92b32a5a55]
[pkrvmbietmlfzoi:36216] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f92b32a5a6f]
[pkrvmbietmlfzoi:36216] [ 8] plumed(+0x13209)[0x564164023209]
[pkrvmbietmlfzoi:36216] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f92b2e2a1ca]
[pkrvmbietmlfzoi:36216] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f92b2e2a28b]
[pkrvmbietmlfzoi:36216] [11] plumed(+0x134a5)[0x5641640234a5]
[pkrvmbietmlfzoi:36216] *** End of error message ***
</pre>
{% endraw %}
