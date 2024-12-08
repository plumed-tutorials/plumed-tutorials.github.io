Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[fv-az1020-777:05977] *** Process received signal ***
[fv-az1020-777:05977] Signal: Aborted (6)
[fv-az1020-777:05977] Signal code:  (-6)
[fv-az1020-777:05977] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3263442520]
[fv-az1020-777:05977] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f32634969fc]
[fv-az1020-777:05977] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3263442476]
[fv-az1020-777:05977] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f32634287f3]
[fv-az1020-777:05977] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f32638a2b9e]
[fv-az1020-777:05977] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f32638ae20c]
[fv-az1020-777:05977] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f32638ae277]
[fv-az1020-777:05977] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f32638ae52b]
[fv-az1020-777:05977] [ 8] plumed(+0x12f48)[0x5560a46f5f48]
[fv-az1020-777:05977] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3263429d90]
[fv-az1020-777:05977] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3263429e40]
[fv-az1020-777:05977] [11] plumed(+0x131e5)[0x5560a46f61e5]
[fv-az1020-777:05977] *** End of error message ***
</pre>
{% endraw %}
