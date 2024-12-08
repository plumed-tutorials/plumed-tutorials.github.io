Stderr for source:  Volumes.md_working_4.dat   
Download: [zipped raw stdout](Volumes.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:05497] *** Process received signal ***
[fv-az1020-777:05497] Signal: Aborted (6)
[fv-az1020-777:05497] Signal code:  (-6)
[fv-az1020-777:05497] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0690642520]
[fv-az1020-777:05497] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f06906969fc]
[fv-az1020-777:05497] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0690642476]
[fv-az1020-777:05497] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f06906287f3]
[fv-az1020-777:05497] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f0690aa2b9e]
[fv-az1020-777:05497] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f0690aae20c]
[fv-az1020-777:05497] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f0690aae277]
[fv-az1020-777:05497] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f0690aae52b]
[fv-az1020-777:05497] [ 8] plumed(+0x12f48)[0x5577e9e1ef48]
[fv-az1020-777:05497] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0690629d90]
[fv-az1020-777:05497] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0690629e40]
[fv-az1020-777:05497] [11] plumed(+0x131e5)[0x5577e9e1f1e5]
[fv-az1020-777:05497] *** End of error message ***
</pre>
{% endraw %}
