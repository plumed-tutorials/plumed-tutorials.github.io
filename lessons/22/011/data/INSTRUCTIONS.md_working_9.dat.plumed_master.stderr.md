Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az573-691:04737] *** Process received signal ***
[fv-az573-691:04737] Signal: Aborted (6)
[fv-az573-691:04737] Signal code:  (-6)
[fv-az573-691:04737] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f55e8a42520]
[fv-az573-691:04737] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f55e8a969fc]
[fv-az573-691:04737] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f55e8a42476]
[fv-az573-691:04737] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f55e8a287f3]
[fv-az573-691:04737] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f55e8ea2b9e]
[fv-az573-691:04737] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f55e8eae20c]
[fv-az573-691:04737] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f55e8eae277]
[fv-az573-691:04737] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f55e8eae52b]
[fv-az573-691:04737] [ 8] plumed_master(+0x14254)[0x55e244fba254]
[fv-az573-691:04737] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f55e8a29d90]
[fv-az573-691:04737] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f55e8a29e40]
[fv-az573-691:04737] [11] plumed_master(+0x14eb5)[0x55e244fbaeb5]
[fv-az573-691:04737] *** End of error message ***
</pre>
{% endraw %}
