Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az665-16:70146] *** Process received signal ***
[fv-az665-16:70146] Signal: Aborted (6)
[fv-az665-16:70146] Signal code:  (-6)
[fv-az665-16:70146] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd819a42520]
[fv-az665-16:70146] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd819a969fc]
[fv-az665-16:70146] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd819a42476]
[fv-az665-16:70146] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd819a287f3]
[fv-az665-16:70146] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd819ea2b9e]
[fv-az665-16:70146] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd819eae20c]
[fv-az665-16:70146] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd819eae277]
[fv-az665-16:70146] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd819eae52b]
[fv-az665-16:70146] [ 8] plumed_master(+0x14254)[0x55b9dd86e254]
[fv-az665-16:70146] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd819a29d90]
[fv-az665-16:70146] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd819a29e40]
[fv-az665-16:70146] [11] plumed_master(+0x14eb5)[0x55b9dd86eeb5]
[fv-az665-16:70146] *** End of error message ***
</pre>
{% endraw %}
