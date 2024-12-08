Stderr for source:  RMSD.md_working_1.dat   
Download: [zipped raw stdout](RMSD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONSTANT with label v : cannot understand the following words from the input line : NCOLS=12, NROWS=2
[fv-az1020-777:06359] *** Process received signal ***
[fv-az1020-777:06359] Signal: Aborted (6)
[fv-az1020-777:06359] Signal code:  (-6)
[fv-az1020-777:06359] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f358b042520]
[fv-az1020-777:06359] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f358b0969fc]
[fv-az1020-777:06359] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f358b042476]
[fv-az1020-777:06359] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f358b0287f3]
[fv-az1020-777:06359] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f358b4a2b9e]
[fv-az1020-777:06359] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f358b4ae20c]
[fv-az1020-777:06359] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f358b4ae277]
[fv-az1020-777:06359] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f358b4ae52b]
[fv-az1020-777:06359] [ 8] plumed(+0x12f48)[0x555f4279df48]
[fv-az1020-777:06359] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f358b029d90]
[fv-az1020-777:06359] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f358b029e40]
[fv-az1020-777:06359] [11] plumed(+0x131e5)[0x555f4279e1e5]
[fv-az1020-777:06359] *** End of error message ***
</pre>
{% endraw %}
