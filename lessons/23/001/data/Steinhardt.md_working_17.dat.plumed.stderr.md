Stderr for source:  Steinhardt.md_working_17.dat   
Download: [zipped raw stdout](Steinhardt.md_working_17.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_17.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:05198] *** Process received signal ***
[fv-az1020-777:05198] Signal: Aborted (6)
[fv-az1020-777:05198] Signal code:  (-6)
[fv-az1020-777:05198] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2b35642520]
[fv-az1020-777:05198] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f2b356969fc]
[fv-az1020-777:05198] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2b35642476]
[fv-az1020-777:05198] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f2b356287f3]
[fv-az1020-777:05198] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f2b35aa2b9e]
[fv-az1020-777:05198] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f2b35aae20c]
[fv-az1020-777:05198] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f2b35aae277]
[fv-az1020-777:05198] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f2b35aae52b]
[fv-az1020-777:05198] [ 8] plumed(+0x12f48)[0x55808ec01f48]
[fv-az1020-777:05198] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2b35629d90]
[fv-az1020-777:05198] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2b35629e40]
[fv-az1020-777:05198] [11] plumed(+0x131e5)[0x55808ec021e5]
[fv-az1020-777:05198] *** End of error message ***
</pre>
{% endraw %}
