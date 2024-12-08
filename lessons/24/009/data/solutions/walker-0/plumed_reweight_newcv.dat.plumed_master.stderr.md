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
[fv-az1778-96:04714] *** Process received signal ***
[fv-az1778-96:04714] Signal: Aborted (6)
[fv-az1778-96:04714] Signal code:  (-6)
[fv-az1778-96:04714] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff8df042520]
[fv-az1778-96:04714] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff8df0969fc]
[fv-az1778-96:04714] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff8df042476]
[fv-az1778-96:04714] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff8df0287f3]
[fv-az1778-96:04714] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff8df4a2b9e]
[fv-az1778-96:04714] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff8df4ae20c]
[fv-az1778-96:04714] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff8df4ae277]
[fv-az1778-96:04714] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff8df4ae52b]
[fv-az1778-96:04714] [ 8] plumed_master(+0x14254)[0x55974d80c254]
[fv-az1778-96:04714] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff8df029d90]
[fv-az1778-96:04714] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff8df029e40]
[fv-az1778-96:04714] [11] plumed_master(+0x14eb5)[0x55974d80ceb5]
[fv-az1778-96:04714] *** End of error message ***
</pre>
{% endraw %}
