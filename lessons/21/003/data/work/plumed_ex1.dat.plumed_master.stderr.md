Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @35 : keyword ARG is compulsory for this action
[fv-az1020-199:05664] *** Process received signal ***
[fv-az1020-199:05664] Signal: Aborted (6)
[fv-az1020-199:05664] Signal code:  (-6)
[fv-az1020-199:05664] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2f61442520]
[fv-az1020-199:05664] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f2f614969fc]
[fv-az1020-199:05664] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2f61442476]
[fv-az1020-199:05664] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f2f614287f3]
[fv-az1020-199:05664] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f2f618a2b9e]
[fv-az1020-199:05664] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f2f618ae20c]
[fv-az1020-199:05664] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f2f618ae277]
[fv-az1020-199:05664] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f2f618ae52b]
[fv-az1020-199:05664] [ 8] plumed_master(+0x14254)[0x556d51bef254]
[fv-az1020-199:05664] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2f61429d90]
[fv-az1020-199:05664] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2f61429e40]
[fv-az1020-199:05664] [11] plumed_master(+0x14eb5)[0x556d51befeb5]
[fv-az1020-199:05664] *** End of error message ***
</pre>
{% endraw %}
