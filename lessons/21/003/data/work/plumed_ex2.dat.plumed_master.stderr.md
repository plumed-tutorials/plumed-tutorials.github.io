Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @38 : keyword ARG is compulsory for this action
[fv-az1251-633:70733] *** Process received signal ***
[fv-az1251-633:70733] Signal: Aborted (6)
[fv-az1251-633:70733] Signal code:  (-6)
[fv-az1251-633:70733] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8257042520]
[fv-az1251-633:70733] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f82570969fc]
[fv-az1251-633:70733] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8257042476]
[fv-az1251-633:70733] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f82570287f3]
[fv-az1251-633:70733] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f82574a2b9e]
[fv-az1251-633:70733] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f82574ae20c]
[fv-az1251-633:70733] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f82574ae277]
[fv-az1251-633:70733] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f82574ae52b]
[fv-az1251-633:70733] [ 8] plumed_master(+0x14254)[0x558d199a3254]
[fv-az1251-633:70733] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8257029d90]
[fv-az1251-633:70733] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8257029e40]
[fv-az1251-633:70733] [11] plumed_master(+0x14eb5)[0x558d199a3eb5]
[fv-az1251-633:70733] *** End of error message ***
</pre>
{% endraw %}
