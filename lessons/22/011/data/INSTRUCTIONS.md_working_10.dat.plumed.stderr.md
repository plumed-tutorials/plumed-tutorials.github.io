Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az1778-96:05346] *** Process received signal ***
[fv-az1778-96:05346] Signal: Aborted (6)
[fv-az1778-96:05346] Signal code:  (-6)
[fv-az1778-96:05346] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3af0242520]
[fv-az1778-96:05346] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3af02969fc]
[fv-az1778-96:05346] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3af0242476]
[fv-az1778-96:05346] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3af02287f3]
[fv-az1778-96:05346] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f3af06a2b9e]
[fv-az1778-96:05346] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f3af06ae20c]
[fv-az1778-96:05346] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f3af06ae277]
[fv-az1778-96:05346] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f3af06ae52b]
[fv-az1778-96:05346] [ 8] plumed(+0x12f48)[0x56099a2e7f48]
[fv-az1778-96:05346] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3af0229d90]
[fv-az1778-96:05346] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3af0229e40]
[fv-az1778-96:05346] [11] plumed(+0x131e5)[0x56099a2e81e5]
[fv-az1778-96:05346] *** End of error message ***
</pre>
{% endraw %}
