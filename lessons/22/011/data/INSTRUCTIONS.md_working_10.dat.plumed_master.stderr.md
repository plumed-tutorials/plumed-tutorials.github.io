Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az1778-96:05355] *** Process received signal ***
[fv-az1778-96:05355] Signal: Aborted (6)
[fv-az1778-96:05355] Signal code:  (-6)
[fv-az1778-96:05355] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6d96442520]
[fv-az1778-96:05355] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6d964969fc]
[fv-az1778-96:05355] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6d96442476]
[fv-az1778-96:05355] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6d964287f3]
[fv-az1778-96:05355] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6d968a2b9e]
[fv-az1778-96:05355] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6d968ae20c]
[fv-az1778-96:05355] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6d968ae277]
[fv-az1778-96:05355] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6d968ae52b]
[fv-az1778-96:05355] [ 8] plumed_master(+0x14254)[0x5587f7eb4254]
[fv-az1778-96:05355] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6d96429d90]
[fv-az1778-96:05355] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6d96429e40]
[fv-az1778-96:05355] [11] plumed_master(+0x14eb5)[0x5587f7eb4eb5]
[fv-az1778-96:05355] *** End of error message ***
</pre>
{% endraw %}
