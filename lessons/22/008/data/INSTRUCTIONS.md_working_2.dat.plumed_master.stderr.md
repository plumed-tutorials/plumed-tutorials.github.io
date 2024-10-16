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
[fv-az1272-281:04953] *** Process received signal ***
[fv-az1272-281:04953] Signal: Aborted (6)
[fv-az1272-281:04953] Signal code:  (-6)
[fv-az1272-281:04953] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2b2b642520]
[fv-az1272-281:04953] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f2b2b6969fc]
[fv-az1272-281:04953] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2b2b642476]
[fv-az1272-281:04953] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f2b2b6287f3]
[fv-az1272-281:04953] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f2b2baa2b9e]
[fv-az1272-281:04953] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f2b2baae20c]
[fv-az1272-281:04953] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f2b2baae277]
[fv-az1272-281:04953] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f2b2baae52b]
[fv-az1272-281:04953] [ 8] plumed_master(+0x14254)[0x558e8aa77254]
[fv-az1272-281:04953] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2b2b629d90]
[fv-az1272-281:04953] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2b2b629e40]
[fv-az1272-281:04953] [11] plumed_master(+0x14eb5)[0x558e8aa77eb5]
[fv-az1272-281:04953] *** End of error message ***
</pre>
{% endraw %}
