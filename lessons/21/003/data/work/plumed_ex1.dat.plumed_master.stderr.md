Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @34 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36589] *** Process received signal ***
[pkrvmbietmlfzoi:36589] Signal: Aborted (6)
[pkrvmbietmlfzoi:36589] Signal code:  (-6)
[pkrvmbietmlfzoi:36589] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff940045330]
[pkrvmbietmlfzoi:36589] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff94009eb2c]
[pkrvmbietmlfzoi:36589] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff94004527e]
[pkrvmbietmlfzoi:36589] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff9400288ff]
[pkrvmbietmlfzoi:36589] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff9404a5ff5]
[pkrvmbietmlfzoi:36589] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff9404bb0da]
[pkrvmbietmlfzoi:36589] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff9404a5a55]
[pkrvmbietmlfzoi:36589] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff9404a5a6f]
[pkrvmbietmlfzoi:36589] [ 8] plumed_master(+0x146dd)[0x5606026476dd]
[pkrvmbietmlfzoi:36589] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff94002a1ca]
[pkrvmbietmlfzoi:36589] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff94002a28b]
[pkrvmbietmlfzoi:36589] [11] plumed_master(+0x15365)[0x560602648365]
[pkrvmbietmlfzoi:36589] *** End of error message ***
</pre>
{% endraw %}
