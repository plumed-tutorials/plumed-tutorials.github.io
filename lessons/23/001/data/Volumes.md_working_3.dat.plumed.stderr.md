Stderr for source:  Volumes.md_working_3.dat   
Download: [zipped raw stdout](Volumes.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1426-552:05613] *** Process received signal ***
[fv-az1426-552:05613] Signal: Aborted (6)
[fv-az1426-552:05613] Signal code:  (-6)
[fv-az1426-552:05613] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f21b5642520]
[fv-az1426-552:05613] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f21b56969fc]
[fv-az1426-552:05613] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f21b5642476]
[fv-az1426-552:05613] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f21b56287f3]
[fv-az1426-552:05613] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f21b5aa2b9e]
[fv-az1426-552:05613] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f21b5aae20c]
[fv-az1426-552:05613] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f21b5aae277]
[fv-az1426-552:05613] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f21b5aae52b]
[fv-az1426-552:05613] [ 8] plumed(+0x12f48)[0x55975d273f48]
[fv-az1426-552:05613] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f21b5629d90]
[fv-az1426-552:05613] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f21b5629e40]
[fv-az1426-552:05613] [11] plumed(+0x131e5)[0x55975d2741e5]
[fv-az1426-552:05613] *** End of error message ***
</pre>
{% endraw %}
