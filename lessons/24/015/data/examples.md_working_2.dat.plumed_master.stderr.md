Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35302] *** Process received signal ***
[pkrvmbietmlfzoi:35302] Signal: Aborted (6)
[pkrvmbietmlfzoi:35302] Signal code:  (-6)
[pkrvmbietmlfzoi:35302] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f934bc45330]
[pkrvmbietmlfzoi:35302] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f934bc9eb2c]
[pkrvmbietmlfzoi:35302] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f934bc4527e]
[pkrvmbietmlfzoi:35302] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f934bc288ff]
[pkrvmbietmlfzoi:35302] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f934c0a5ff5]
[pkrvmbietmlfzoi:35302] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f934c0bb0da]
[pkrvmbietmlfzoi:35302] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f934c0a5a55]
[pkrvmbietmlfzoi:35302] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f934c0a5a6f]
[pkrvmbietmlfzoi:35302] [ 8] plumed_master(+0x146dd)[0x55f570d6e6dd]
[pkrvmbietmlfzoi:35302] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f934bc2a1ca]
[pkrvmbietmlfzoi:35302] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f934bc2a28b]
[pkrvmbietmlfzoi:35302] [11] plumed_master(+0x15365)[0x55f570d6f365]
[pkrvmbietmlfzoi:35302] *** End of error message ***
</pre>
{% endraw %}
