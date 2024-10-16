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
[fv-az1020-199:05729] *** Process received signal ***
[fv-az1020-199:05729] Signal: Aborted (6)
[fv-az1020-199:05729] Signal code:  (-6)
[fv-az1020-199:05729] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7facf8442520]
[fv-az1020-199:05729] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7facf84969fc]
[fv-az1020-199:05729] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7facf8442476]
[fv-az1020-199:05729] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7facf84287f3]
[fv-az1020-199:05729] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7facf88a2b9e]
[fv-az1020-199:05729] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7facf88ae20c]
[fv-az1020-199:05729] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7facf88ae277]
[fv-az1020-199:05729] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7facf88ae52b]
[fv-az1020-199:05729] [ 8] plumed_master(+0x14254)[0x5617220f3254]
[fv-az1020-199:05729] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7facf8429d90]
[fv-az1020-199:05729] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7facf8429e40]
[fv-az1020-199:05729] [11] plumed_master(+0x14eb5)[0x5617220f3eb5]
[fv-az1020-199:05729] *** End of error message ***
</pre>
{% endraw %}
