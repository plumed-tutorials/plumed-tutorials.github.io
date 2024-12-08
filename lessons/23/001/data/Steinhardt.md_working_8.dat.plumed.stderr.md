Stderr for source:  Steinhardt.md_working_8.dat   
Download: [zipped raw stdout](Steinhardt.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:04994] *** Process received signal ***
[fv-az1020-777:04994] Signal: Aborted (6)
[fv-az1020-777:04994] Signal code:  (-6)
[fv-az1020-777:04994] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3defa42520]
[fv-az1020-777:04994] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f3defa969fc]
[fv-az1020-777:04994] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3defa42476]
[fv-az1020-777:04994] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f3defa287f3]
[fv-az1020-777:04994] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f3defea2b9e]
[fv-az1020-777:04994] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f3defeae20c]
[fv-az1020-777:04994] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f3defeae277]
[fv-az1020-777:04994] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f3defeae52b]
[fv-az1020-777:04994] [ 8] plumed(+0x12f48)[0x55e01a113f48]
[fv-az1020-777:04994] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3defa29d90]
[fv-az1020-777:04994] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3defa29e40]
[fv-az1020-777:04994] [11] plumed(+0x131e5)[0x55e01a1141e5]
[fv-az1020-777:04994] *** End of error message ***
</pre>
{% endraw %}
