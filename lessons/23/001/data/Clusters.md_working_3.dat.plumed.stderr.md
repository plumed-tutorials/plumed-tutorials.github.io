Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1020-777:06328] *** Process received signal ***
[fv-az1020-777:06328] Signal: Aborted (6)
[fv-az1020-777:06328] Signal code:  (-6)
[fv-az1020-777:06328] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f73f8842520]
[fv-az1020-777:06328] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f73f88969fc]
[fv-az1020-777:06328] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f73f8842476]
[fv-az1020-777:06328] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f73f88287f3]
[fv-az1020-777:06328] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f73f8ca2b9e]
[fv-az1020-777:06328] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f73f8cae20c]
[fv-az1020-777:06328] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f73f8cae277]
[fv-az1020-777:06328] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f73f8cae52b]
[fv-az1020-777:06328] [ 8] plumed(+0x12f48)[0x558f5b0e7f48]
[fv-az1020-777:06328] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f73f8829d90]
[fv-az1020-777:06328] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f73f8829e40]
[fv-az1020-777:06328] [11] plumed(+0x131e5)[0x558f5b0e81e5]
[fv-az1020-777:06328] *** End of error message ***
</pre>
{% endraw %}