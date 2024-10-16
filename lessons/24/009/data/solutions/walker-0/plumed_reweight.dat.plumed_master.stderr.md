Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1020-199:04222] *** Process received signal ***
[fv-az1020-199:04222] Signal: Aborted (6)
[fv-az1020-199:04222] Signal code:  (-6)
[fv-az1020-199:04222] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f488f042520]
[fv-az1020-199:04222] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f488f0969fc]
[fv-az1020-199:04222] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f488f042476]
[fv-az1020-199:04222] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f488f0287f3]
[fv-az1020-199:04222] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f488f4a2b9e]
[fv-az1020-199:04222] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f488f4ae20c]
[fv-az1020-199:04222] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f488f4ae277]
[fv-az1020-199:04222] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f488f4ae52b]
[fv-az1020-199:04222] [ 8] plumed_master(+0x14254)[0x56249ee4b254]
[fv-az1020-199:04222] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f488f029d90]
[fv-az1020-199:04222] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f488f029e40]
[fv-az1020-199:04222] [11] plumed_master(+0x14eb5)[0x56249ee4beb5]
[fv-az1020-199:04222] *** End of error message ***
</pre>
{% endraw %}
