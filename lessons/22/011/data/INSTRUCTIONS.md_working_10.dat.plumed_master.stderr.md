Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az573-691:04760] *** Process received signal ***
[fv-az573-691:04760] Signal: Aborted (6)
[fv-az573-691:04760] Signal code:  (-6)
[fv-az573-691:04760] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fcadf242520]
[fv-az573-691:04760] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fcadf2969fc]
[fv-az573-691:04760] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fcadf242476]
[fv-az573-691:04760] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fcadf2287f3]
[fv-az573-691:04760] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fcadf6a2b9e]
[fv-az573-691:04760] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fcadf6ae20c]
[fv-az573-691:04760] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fcadf6ae277]
[fv-az573-691:04760] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fcadf6ae52b]
[fv-az573-691:04760] [ 8] plumed_master(+0x14254)[0x55ee97e92254]
[fv-az573-691:04760] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fcadf229d90]
[fv-az573-691:04760] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fcadf229e40]
[fv-az573-691:04760] [11] plumed_master(+0x14eb5)[0x55ee97e92eb5]
[fv-az573-691:04760] *** End of error message ***
</pre>
{% endraw %}
