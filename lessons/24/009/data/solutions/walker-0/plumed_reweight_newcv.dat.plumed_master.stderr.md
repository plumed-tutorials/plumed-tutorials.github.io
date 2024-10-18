Stderr for source:  ./solutions/walker-0/plumed_reweight_newcv.dat   
Download: [zipped raw stdout](plumed_reweight_newcv.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight_newcv.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1251-633:69424] *** Process received signal ***
[fv-az1251-633:69424] Signal: Aborted (6)
[fv-az1251-633:69424] Signal code:  (-6)
[fv-az1251-633:69424] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7efc16c42520]
[fv-az1251-633:69424] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7efc16c969fc]
[fv-az1251-633:69424] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7efc16c42476]
[fv-az1251-633:69424] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7efc16c287f3]
[fv-az1251-633:69424] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7efc170a2b9e]
[fv-az1251-633:69424] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7efc170ae20c]
[fv-az1251-633:69424] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7efc170ae277]
[fv-az1251-633:69424] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7efc170ae52b]
[fv-az1251-633:69424] [ 8] plumed_master(+0x14254)[0x558f52a7c254]
[fv-az1251-633:69424] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7efc16c29d90]
[fv-az1251-633:69424] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7efc16c29e40]
[fv-az1251-633:69424] [11] plumed_master(+0x14eb5)[0x558f52a7ceb5]
[fv-az1251-633:69424] *** End of error message ***
</pre>
{% endraw %}
