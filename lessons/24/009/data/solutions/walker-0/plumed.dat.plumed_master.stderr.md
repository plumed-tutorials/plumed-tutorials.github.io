Stderr for source:  ./solutions/walker-0/plumed.dat   
Download: [zipped raw stdout](plumed.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action HBOND_MATRIX with label hbmat1 : cannot understand the following words from the input line : SUM
[fv-az1251-633:69372] *** Process received signal ***
[fv-az1251-633:69372] Signal: Aborted (6)
[fv-az1251-633:69372] Signal code:  (-6)
[fv-az1251-633:69372] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa494a42520]
[fv-az1251-633:69372] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa494a969fc]
[fv-az1251-633:69372] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa494a42476]
[fv-az1251-633:69372] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa494a287f3]
[fv-az1251-633:69372] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa494ea2b9e]
[fv-az1251-633:69372] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa494eae20c]
[fv-az1251-633:69372] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa494eae277]
[fv-az1251-633:69372] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa494eae52b]
[fv-az1251-633:69372] [ 8] plumed_master(+0x14254)[0x55e98e16c254]
[fv-az1251-633:69372] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa494a29d90]
[fv-az1251-633:69372] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa494a29e40]
[fv-az1251-633:69372] [11] plumed_master(+0x14eb5)[0x55e98e16ceb5]
[fv-az1251-633:69372] *** End of error message ***
</pre>
{% endraw %}
