Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1251-633:70776] *** Process received signal ***
[fv-az1251-633:70776] Signal: Aborted (6)
[fv-az1251-633:70776] Signal code:  (-6)
[fv-az1251-633:70776] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0831842520]
[fv-az1251-633:70776] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f08318969fc]
[fv-az1251-633:70776] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0831842476]
[fv-az1251-633:70776] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f08318287f3]
[fv-az1251-633:70776] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f0831ca2b9e]
[fv-az1251-633:70776] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f0831cae20c]
[fv-az1251-633:70776] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f0831cae277]
[fv-az1251-633:70776] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f0831cae52b]
[fv-az1251-633:70776] [ 8] plumed_master(+0x14254)[0x55d7c4ffb254]
[fv-az1251-633:70776] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0831829d90]
[fv-az1251-633:70776] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0831829e40]
[fv-az1251-633:70776] [11] plumed_master(+0x14eb5)[0x55d7c4ffbeb5]
[fv-az1251-633:70776] *** End of error message ***
</pre>
{% endraw %}
