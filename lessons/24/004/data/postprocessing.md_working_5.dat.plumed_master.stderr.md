Stderr for source:  postprocessing.md_working_5.dat   
Download: [zipped raw stdout](postprocessing.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @18 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36063] *** Process received signal ***
[pkrvmbietmlfzoi:36063] Signal: Aborted (6)
[pkrvmbietmlfzoi:36063] Signal code:  (-6)
[pkrvmbietmlfzoi:36063] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb4adc45330]
[pkrvmbietmlfzoi:36063] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb4adc9eb2c]
[pkrvmbietmlfzoi:36063] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb4adc4527e]
[pkrvmbietmlfzoi:36063] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb4adc288ff]
[pkrvmbietmlfzoi:36063] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb4ae0a5ff5]
[pkrvmbietmlfzoi:36063] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb4ae0bb0da]
[pkrvmbietmlfzoi:36063] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb4ae0a5a55]
[pkrvmbietmlfzoi:36063] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb4ae0a5a6f]
[pkrvmbietmlfzoi:36063] [ 8] plumed_master(+0x146dd)[0x5619d09886dd]
[pkrvmbietmlfzoi:36063] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb4adc2a1ca]
[pkrvmbietmlfzoi:36063] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb4adc2a28b]
[pkrvmbietmlfzoi:36063] [11] plumed_master(+0x15365)[0x5619d0989365]
[pkrvmbietmlfzoi:36063] *** End of error message ***
</pre>
{% endraw %}
