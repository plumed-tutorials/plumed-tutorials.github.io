Stderr for source:  work/plumed_ex6.dat   
Download: [zipped raw stdout](plumed_ex6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @53 : keyword ARG is compulsory for this action
[fv-az1251-633:70959] *** Process received signal ***
[fv-az1251-633:70959] Signal: Aborted (6)
[fv-az1251-633:70959] Signal code:  (-6)
[fv-az1251-633:70959] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe5db442520]
[fv-az1251-633:70959] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe5db4969fc]
[fv-az1251-633:70959] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe5db442476]
[fv-az1251-633:70959] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe5db4287f3]
[fv-az1251-633:70959] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe5db8a2b9e]
[fv-az1251-633:70959] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe5db8ae20c]
[fv-az1251-633:70959] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe5db8ae277]
[fv-az1251-633:70959] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe5db8ae52b]
[fv-az1251-633:70959] [ 8] plumed_master(+0x14254)[0x55d351239254]
[fv-az1251-633:70959] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe5db429d90]
[fv-az1251-633:70959] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe5db429e40]
[fv-az1251-633:70959] [11] plumed_master(+0x14eb5)[0x55d351239eb5]
[fv-az1251-633:70959] *** End of error message ***
</pre>
{% endraw %}
