Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[pkrvmbietmlfzoi:35299] *** Process received signal ***
[pkrvmbietmlfzoi:35299] Signal: Aborted (6)
[pkrvmbietmlfzoi:35299] Signal code:  (-6)
[pkrvmbietmlfzoi:35299] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc3cba45330]
[pkrvmbietmlfzoi:35299] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc3cba9eb2c]
[pkrvmbietmlfzoi:35299] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc3cba4527e]
[pkrvmbietmlfzoi:35299] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc3cba288ff]
[pkrvmbietmlfzoi:35299] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc3cbea5ff5]
[pkrvmbietmlfzoi:35299] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc3cbebb0da]
[pkrvmbietmlfzoi:35299] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc3cbea5a55]
[pkrvmbietmlfzoi:35299] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc3cbea5a6f]
[pkrvmbietmlfzoi:35299] [ 8] plumed(+0x13209)[0x56325fab5209]
[pkrvmbietmlfzoi:35299] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc3cba2a1ca]
[pkrvmbietmlfzoi:35299] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc3cba2a28b]
[pkrvmbietmlfzoi:35299] [11] plumed(+0x134a5)[0x56325fab54a5]
[pkrvmbietmlfzoi:35299] *** End of error message ***
</pre>
{% endraw %}
