Stderr for source:  Tasks.md_working_1.dat   
Download: [zipped raw stdout](Tasks.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1020-777:04615] *** Process received signal ***
[fv-az1020-777:04615] Signal: Aborted (6)
[fv-az1020-777:04615] Signal code:  (-6)
[fv-az1020-777:04615] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f7536c42520]
[fv-az1020-777:04615] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f7536c969fc]
[fv-az1020-777:04615] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f7536c42476]
[fv-az1020-777:04615] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f7536c287f3]
[fv-az1020-777:04615] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f75370a2b9e]
[fv-az1020-777:04615] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f75370ae20c]
[fv-az1020-777:04615] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f75370ae277]
[fv-az1020-777:04615] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f75370ae52b]
[fv-az1020-777:04615] [ 8] plumed(+0x12f48)[0x557fce8cbf48]
[fv-az1020-777:04615] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f7536c29d90]
[fv-az1020-777:04615] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f7536c29e40]
[fv-az1020-777:04615] [11] plumed(+0x131e5)[0x557fce8cc1e5]
[fv-az1020-777:04615] *** End of error message ***
</pre>
{% endraw %}
