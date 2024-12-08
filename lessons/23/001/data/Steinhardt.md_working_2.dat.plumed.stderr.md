Stderr for source:  Steinhardt.md_working_2.dat   
Download: [zipped raw stdout](Steinhardt.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:04856] *** Process received signal ***
[fv-az1020-777:04856] Signal: Aborted (6)
[fv-az1020-777:04856] Signal code:  (-6)
[fv-az1020-777:04856] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f5cfa842520]
[fv-az1020-777:04856] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f5cfa8969fc]
[fv-az1020-777:04856] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f5cfa842476]
[fv-az1020-777:04856] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f5cfa8287f3]
[fv-az1020-777:04856] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f5cfaca2b9e]
[fv-az1020-777:04856] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f5cfacae20c]
[fv-az1020-777:04856] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f5cfacae277]
[fv-az1020-777:04856] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f5cfacae52b]
[fv-az1020-777:04856] [ 8] plumed(+0x12f48)[0x5643a82c3f48]
[fv-az1020-777:04856] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f5cfa829d90]
[fv-az1020-777:04856] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f5cfa829e40]
[fv-az1020-777:04856] [11] plumed(+0x131e5)[0x5643a82c41e5]
[fv-az1020-777:04856] *** End of error message ***
</pre>
{% endraw %}
