Stderr for source:  Behler.md_working_4.dat   
Download: [zipped raw stdout](Behler.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1020-777:05342] *** Process received signal ***
[fv-az1020-777:05342] Signal: Aborted (6)
[fv-az1020-777:05342] Signal code:  (-6)
[fv-az1020-777:05342] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd817a42520]
[fv-az1020-777:05342] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd817a969fc]
[fv-az1020-777:05342] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd817a42476]
[fv-az1020-777:05342] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd817a287f3]
[fv-az1020-777:05342] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd817ea2b9e]
[fv-az1020-777:05342] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd817eae20c]
[fv-az1020-777:05342] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd817eae277]
[fv-az1020-777:05342] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd817eae52b]
[fv-az1020-777:05342] [ 8] plumed(+0x12f48)[0x563c1dc2ff48]
[fv-az1020-777:05342] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd817a29d90]
[fv-az1020-777:05342] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd817a29e40]
[fv-az1020-777:05342] [11] plumed(+0x131e5)[0x563c1dc301e5]
[fv-az1020-777:05342] *** End of error message ***
</pre>
{% endraw %}
