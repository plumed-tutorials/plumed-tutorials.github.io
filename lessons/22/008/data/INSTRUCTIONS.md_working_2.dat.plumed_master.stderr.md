Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[fv-az1429-301:04554] *** Process received signal ***
[fv-az1429-301:04554] Signal: Aborted (6)
[fv-az1429-301:04554] Signal code:  (-6)
[fv-az1429-301:04554] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc47a642520]
[fv-az1429-301:04554] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc47a6969fc]
[fv-az1429-301:04554] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc47a642476]
[fv-az1429-301:04554] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc47a6287f3]
[fv-az1429-301:04554] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc47aaa2b9e]
[fv-az1429-301:04554] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc47aaae20c]
[fv-az1429-301:04554] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc47aaae277]
[fv-az1429-301:04554] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc47aaae52b]
[fv-az1429-301:04554] [ 8] plumed_master(+0x14254)[0x558a3cf31254]
[fv-az1429-301:04554] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc47a629d90]
[fv-az1429-301:04554] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc47a629e40]
[fv-az1429-301:04554] [11] plumed_master(+0x14eb5)[0x558a3cf31eb5]
[fv-az1429-301:04554] *** End of error message ***
</pre>
{% endraw %}
