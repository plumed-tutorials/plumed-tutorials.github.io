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
[fv-az1020-777:05461] *** Process received signal ***
[fv-az1020-777:05461] Signal: Aborted (6)
[fv-az1020-777:05461] Signal code:  (-6)
[fv-az1020-777:05461] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fea30a42520]
[fv-az1020-777:05461] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fea30a969fc]
[fv-az1020-777:05461] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fea30a42476]
[fv-az1020-777:05461] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fea30a287f3]
[fv-az1020-777:05461] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fea30ea2b9e]
[fv-az1020-777:05461] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fea30eae20c]
[fv-az1020-777:05461] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fea30eae277]
[fv-az1020-777:05461] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fea30eae52b]
[fv-az1020-777:05461] [ 8] plumed(+0x12f48)[0x5619a77ddf48]
[fv-az1020-777:05461] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fea30a29d90]
[fv-az1020-777:05461] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fea30a29e40]
[fv-az1020-777:05461] [11] plumed(+0x131e5)[0x5619a77de1e5]
[fv-az1020-777:05461] *** End of error message ***
</pre>
{% endraw %}