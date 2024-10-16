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
[fv-az1020-199:04191] *** Process received signal ***
[fv-az1020-199:04191] Signal: Aborted (6)
[fv-az1020-199:04191] Signal code:  (-6)
[fv-az1020-199:04191] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7efed8842520]
[fv-az1020-199:04191] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7efed88969fc]
[fv-az1020-199:04191] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7efed8842476]
[fv-az1020-199:04191] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7efed88287f3]
[fv-az1020-199:04191] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7efed8ca2b9e]
[fv-az1020-199:04191] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7efed8cae20c]
[fv-az1020-199:04191] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7efed8cae277]
[fv-az1020-199:04191] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7efed8cae52b]
[fv-az1020-199:04191] [ 8] plumed_master(+0x14254)[0x563c0d76b254]
[fv-az1020-199:04191] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7efed8829d90]
[fv-az1020-199:04191] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7efed8829e40]
[fv-az1020-199:04191] [11] plumed_master(+0x14eb5)[0x563c0d76beb5]
[fv-az1020-199:04191] *** End of error message ***
</pre>
{% endraw %}
