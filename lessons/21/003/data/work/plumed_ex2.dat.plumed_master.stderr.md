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
[fv-az1778-96:05492] *** Process received signal ***
[fv-az1778-96:05492] Signal: Aborted (6)
[fv-az1778-96:05492] Signal code:  (-6)
[fv-az1778-96:05492] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fac1c442520]
[fv-az1778-96:05492] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fac1c4969fc]
[fv-az1778-96:05492] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fac1c442476]
[fv-az1778-96:05492] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fac1c4287f3]
[fv-az1778-96:05492] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fac1c8a2b9e]
[fv-az1778-96:05492] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fac1c8ae20c]
[fv-az1778-96:05492] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fac1c8ae277]
[fv-az1778-96:05492] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fac1c8ae52b]
[fv-az1778-96:05492] [ 8] plumed_master(+0x14254)[0x55ffa36fd254]
[fv-az1778-96:05492] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fac1c429d90]
[fv-az1778-96:05492] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fac1c429e40]
[fv-az1778-96:05492] [11] plumed_master(+0x14eb5)[0x55ffa36fdeb5]
[fv-az1778-96:05492] *** End of error message ***
</pre>
{% endraw %}
