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
[fv-az1530-405:69868] *** Process received signal ***
[fv-az1530-405:69868] Signal: Aborted (6)
[fv-az1530-405:69868] Signal code:  (-6)
[fv-az1530-405:69868] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7faa24642520]
[fv-az1530-405:69868] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7faa246969fc]
[fv-az1530-405:69868] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7faa24642476]
[fv-az1530-405:69868] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7faa246287f3]
[fv-az1530-405:69868] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7faa24aa2b9e]
[fv-az1530-405:69868] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7faa24aae20c]
[fv-az1530-405:69868] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7faa24aae277]
[fv-az1530-405:69868] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7faa24aae52b]
[fv-az1530-405:69868] [ 8] plumed_master(+0x14254)[0x56166fa8d254]
[fv-az1530-405:69868] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7faa24629d90]
[fv-az1530-405:69868] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7faa24629e40]
[fv-az1530-405:69868] [11] plumed_master(+0x14eb5)[0x56166fa8deb5]
[fv-az1530-405:69868] *** End of error message ***
</pre>
{% endraw %}
