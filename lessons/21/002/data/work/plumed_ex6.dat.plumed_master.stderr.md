Stderr for source:  work/plumed_ex6.dat   
Download: [zipped raw stdout](plumed_ex6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @53 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36858] *** Process received signal ***
[pkrvmbietmlfzoi:36858] Signal: Aborted (6)
[pkrvmbietmlfzoi:36858] Signal code:  (-6)
[pkrvmbietmlfzoi:36858] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5534e45330]
[pkrvmbietmlfzoi:36858] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5534e9eb2c]
[pkrvmbietmlfzoi:36858] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5534e4527e]
[pkrvmbietmlfzoi:36858] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5534e288ff]
[pkrvmbietmlfzoi:36858] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f55352a5ff5]
[pkrvmbietmlfzoi:36858] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f55352bb0da]
[pkrvmbietmlfzoi:36858] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f55352a5a55]
[pkrvmbietmlfzoi:36858] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f55352a5a6f]
[pkrvmbietmlfzoi:36858] [ 8] plumed_master(+0x146dd)[0x555bc7bc06dd]
[pkrvmbietmlfzoi:36858] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5534e2a1ca]
[pkrvmbietmlfzoi:36858] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5534e2a28b]
[pkrvmbietmlfzoi:36858] [11] plumed_master(+0x15365)[0x555bc7bc1365]
[pkrvmbietmlfzoi:36858] *** End of error message ***
</pre>
{% endraw %}
