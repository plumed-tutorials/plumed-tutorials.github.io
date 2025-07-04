Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35378] *** Process received signal ***
[pkrvmbietmlfzoi:35378] Signal: Aborted (6)
[pkrvmbietmlfzoi:35378] Signal code:  (-6)
[pkrvmbietmlfzoi:35378] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7a42645330]
[pkrvmbietmlfzoi:35378] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7a4269eb2c]
[pkrvmbietmlfzoi:35378] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7a4264527e]
[pkrvmbietmlfzoi:35378] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7a426288ff]
[pkrvmbietmlfzoi:35378] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7a42aa5ff5]
[pkrvmbietmlfzoi:35378] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7a42abb0da]
[pkrvmbietmlfzoi:35378] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7a42aa5a55]
[pkrvmbietmlfzoi:35378] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7a42aa5a6f]
[pkrvmbietmlfzoi:35378] [ 8] plumed(+0x13209)[0x560c0512f209]
[pkrvmbietmlfzoi:35378] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7a4262a1ca]
[pkrvmbietmlfzoi:35378] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7a4262a28b]
[pkrvmbietmlfzoi:35378] [11] plumed(+0x134a5)[0x560c0512f4a5]
[pkrvmbietmlfzoi:35378] *** End of error message ***
</pre>
{% endraw %}
