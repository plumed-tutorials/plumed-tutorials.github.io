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
[fv-az1251-633:71002] *** Process received signal ***
[fv-az1251-633:71002] Signal: Aborted (6)
[fv-az1251-633:71002] Signal code:  (-6)
[fv-az1251-633:71002] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6402242520]
[fv-az1251-633:71002] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f64022969fc]
[fv-az1251-633:71002] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6402242476]
[fv-az1251-633:71002] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f64022287f3]
[fv-az1251-633:71002] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f64026a2b9e]
[fv-az1251-633:71002] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f64026ae20c]
[fv-az1251-633:71002] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f64026ae277]
[fv-az1251-633:71002] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f64026ae52b]
[fv-az1251-633:71002] [ 8] plumed_master(+0x14254)[0x55f0637e4254]
[fv-az1251-633:71002] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6402229d90]
[fv-az1251-633:71002] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6402229e40]
[fv-az1251-633:71002] [11] plumed_master(+0x14eb5)[0x55f0637e4eb5]
[fv-az1251-633:71002] *** End of error message ***
</pre>
{% endraw %}
