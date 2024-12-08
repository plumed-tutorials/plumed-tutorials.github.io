Stderr for source:  Behler.md_working_1.dat   
Download: [zipped raw stdout](Behler.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:05271] *** Process received signal ***
[fv-az1020-777:05271] Signal: Aborted (6)
[fv-az1020-777:05271] Signal code:  (-6)
[fv-az1020-777:05271] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd931642520]
[fv-az1020-777:05271] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd9316969fc]
[fv-az1020-777:05271] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd931642476]
[fv-az1020-777:05271] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd9316287f3]
[fv-az1020-777:05271] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd931aa2b9e]
[fv-az1020-777:05271] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd931aae20c]
[fv-az1020-777:05271] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd931aae277]
[fv-az1020-777:05271] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd931aae52b]
[fv-az1020-777:05271] [ 8] plumed(+0x12f48)[0x55a871f41f48]
[fv-az1020-777:05271] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd931629d90]
[fv-az1020-777:05271] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd931629e40]
[fv-az1020-777:05271] [11] plumed(+0x131e5)[0x55a871f421e5]
[fv-az1020-777:05271] *** End of error message ***
</pre>
{% endraw %}
