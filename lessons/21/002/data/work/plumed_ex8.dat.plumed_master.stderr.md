Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @49 : keyword ARG is compulsory for this action
[fv-az1272-281:05501] *** Process received signal ***
[fv-az1272-281:05501] Signal: Aborted (6)
[fv-az1272-281:05501] Signal code:  (-6)
[fv-az1272-281:05501] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f59e2242520]
[fv-az1272-281:05501] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f59e22969fc]
[fv-az1272-281:05501] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f59e2242476]
[fv-az1272-281:05501] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f59e22287f3]
[fv-az1272-281:05501] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f59e26a2b9e]
[fv-az1272-281:05501] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f59e26ae20c]
[fv-az1272-281:05501] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f59e26ae277]
[fv-az1272-281:05501] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f59e26ae52b]
[fv-az1272-281:05501] [ 8] plumed_master(+0x14254)[0x55daf6ea6254]
[fv-az1272-281:05501] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f59e2229d90]
[fv-az1272-281:05501] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f59e2229e40]
[fv-az1272-281:05501] [11] plumed_master(+0x14eb5)[0x55daf6ea6eb5]
[fv-az1272-281:05501] *** End of error message ***
</pre>
{% endraw %}
