Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1020-777:04143] *** Process received signal ***
[fv-az1020-777:04143] Signal: Aborted (6)
[fv-az1020-777:04143] Signal code:  (-6)
[fv-az1020-777:04143] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8638c42520]
[fv-az1020-777:04143] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8638c969fc]
[fv-az1020-777:04143] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8638c42476]
[fv-az1020-777:04143] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8638c287f3]
[fv-az1020-777:04143] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f86390a2b9e]
[fv-az1020-777:04143] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f86390ae20c]
[fv-az1020-777:04143] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f86390ae277]
[fv-az1020-777:04143] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f86390ae52b]
[fv-az1020-777:04143] [ 8] plumed(+0x12f48)[0x55f0d18adf48]
[fv-az1020-777:04143] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8638c29d90]
[fv-az1020-777:04143] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8638c29e40]
[fv-az1020-777:04143] [11] plumed(+0x131e5)[0x55f0d18ae1e5]
[fv-az1020-777:04143] *** End of error message ***
</pre>
{% endraw %}
