Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action CUSTOM_VECTOR with label s1_sp : first argument to this action must be a vector
[pkrvmbietmlfzoi:35202] *** Process received signal ***
[pkrvmbietmlfzoi:35202] Signal: Aborted (6)
[pkrvmbietmlfzoi:35202] Signal code:  (-6)
[pkrvmbietmlfzoi:35202] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4694a45330]
[pkrvmbietmlfzoi:35202] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4694a9eb2c]
[pkrvmbietmlfzoi:35202] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4694a4527e]
[pkrvmbietmlfzoi:35202] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4694a288ff]
[pkrvmbietmlfzoi:35202] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4694ea5ff5]
[pkrvmbietmlfzoi:35202] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4694ebb0da]
[pkrvmbietmlfzoi:35202] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4694ea5a55]
[pkrvmbietmlfzoi:35202] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4694ea5a6f]
[pkrvmbietmlfzoi:35202] [ 8] plumed_master(+0x146dd)[0x556ade0d56dd]
[pkrvmbietmlfzoi:35202] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4694a2a1ca]
[pkrvmbietmlfzoi:35202] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4694a2a28b]
[pkrvmbietmlfzoi:35202] [11] plumed_master(+0x15365)[0x556ade0d6365]
[pkrvmbietmlfzoi:35202] *** End of error message ***
</pre>
{% endraw %}
