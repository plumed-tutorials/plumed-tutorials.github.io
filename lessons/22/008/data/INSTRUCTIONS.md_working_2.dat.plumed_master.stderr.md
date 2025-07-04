Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:35548] *** Process received signal ***
[pkrvmbietmlfzoi:35548] Signal: Aborted (6)
[pkrvmbietmlfzoi:35548] Signal code:  (-6)
[pkrvmbietmlfzoi:35548] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f82baa45330]
[pkrvmbietmlfzoi:35548] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f82baa9eb2c]
[pkrvmbietmlfzoi:35548] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f82baa4527e]
[pkrvmbietmlfzoi:35548] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f82baa288ff]
[pkrvmbietmlfzoi:35548] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f82baea5ff5]
[pkrvmbietmlfzoi:35548] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f82baebb0da]
[pkrvmbietmlfzoi:35548] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f82baea5a55]
[pkrvmbietmlfzoi:35548] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f82baea5a6f]
[pkrvmbietmlfzoi:35548] [ 8] plumed_master(+0x146dd)[0x556d1fcff6dd]
[pkrvmbietmlfzoi:35548] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f82baa2a1ca]
[pkrvmbietmlfzoi:35548] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f82baa2a28b]
[pkrvmbietmlfzoi:35548] [11] plumed_master(+0x15365)[0x556d1fd00365]
[pkrvmbietmlfzoi:35548] *** End of error message ***
</pre>
{% endraw %}
