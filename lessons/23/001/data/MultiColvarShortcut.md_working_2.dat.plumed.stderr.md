Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1020-777:04277] *** Process received signal ***
[fv-az1020-777:04277] Signal: Aborted (6)
[fv-az1020-777:04277] Signal code:  (-6)
[fv-az1020-777:04277] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6616a42520]
[fv-az1020-777:04277] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6616a969fc]
[fv-az1020-777:04277] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6616a42476]
[fv-az1020-777:04277] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6616a287f3]
[fv-az1020-777:04277] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6616ea2b9e]
[fv-az1020-777:04277] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6616eae20c]
[fv-az1020-777:04277] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6616eae277]
[fv-az1020-777:04277] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6616eae52b]
[fv-az1020-777:04277] [ 8] plumed(+0x12f48)[0x556c75505f48]
[fv-az1020-777:04277] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6616a29d90]
[fv-az1020-777:04277] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6616a29e40]
[fv-az1020-777:04277] [11] plumed(+0x131e5)[0x556c755061e5]
[fv-az1020-777:04277] *** End of error message ***
</pre>
{% endraw %}
