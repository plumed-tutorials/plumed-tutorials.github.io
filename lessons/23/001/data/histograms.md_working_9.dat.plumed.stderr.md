Stderr for source:  histograms.md_working_9.dat   
Download: [zipped raw stdout](histograms.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[fv-az1020-777:06165] *** Process received signal ***
[fv-az1020-777:06165] Signal: Aborted (6)
[fv-az1020-777:06165] Signal code:  (-6)
[fv-az1020-777:06165] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f495a042520]
[fv-az1020-777:06165] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f495a0969fc]
[fv-az1020-777:06165] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f495a042476]
[fv-az1020-777:06165] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f495a0287f3]
[fv-az1020-777:06165] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f495a4a2b9e]
[fv-az1020-777:06165] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f495a4ae20c]
[fv-az1020-777:06165] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f495a4ae277]
[fv-az1020-777:06165] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f495a4ae52b]
[fv-az1020-777:06165] [ 8] plumed(+0x12f48)[0x564162a8df48]
[fv-az1020-777:06165] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f495a029d90]
[fv-az1020-777:06165] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f495a029e40]
[fv-az1020-777:06165] [11] plumed(+0x131e5)[0x564162a8e1e5]
[fv-az1020-777:06165] *** End of error message ***
</pre>
{% endraw %}