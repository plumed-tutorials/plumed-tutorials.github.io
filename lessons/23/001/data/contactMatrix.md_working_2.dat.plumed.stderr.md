Stderr for source:  contactMatrix.md_working_2.dat   
Download: [zipped raw stdout](contactMatrix.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1020-777:04397] *** Process received signal ***
[fv-az1020-777:04397] Signal: Aborted (6)
[fv-az1020-777:04397] Signal code:  (-6)
[fv-az1020-777:04397] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f07de442520]
[fv-az1020-777:04397] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f07de4969fc]
[fv-az1020-777:04397] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f07de442476]
[fv-az1020-777:04397] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f07de4287f3]
[fv-az1020-777:04397] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f07de8a2b9e]
[fv-az1020-777:04397] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f07de8ae20c]
[fv-az1020-777:04397] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f07de8ae277]
[fv-az1020-777:04397] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f07de8ae52b]
[fv-az1020-777:04397] [ 8] plumed(+0x12f48)[0x560f29565f48]
[fv-az1020-777:04397] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f07de429d90]
[fv-az1020-777:04397] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f07de429e40]
[fv-az1020-777:04397] [11] plumed(+0x131e5)[0x560f295661e5]
[fv-az1020-777:04397] *** End of error message ***
</pre>
{% endraw %}
