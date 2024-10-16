Stderr for source:  histograms.md_working_5.dat   
Download: [zipped raw stdout](histograms.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1426-552:06154] *** Process received signal ***
[fv-az1426-552:06154] Signal: Aborted (6)
[fv-az1426-552:06154] Signal code:  (-6)
[fv-az1426-552:06154] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe7e3e42520]
[fv-az1426-552:06154] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe7e3e969fc]
[fv-az1426-552:06154] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe7e3e42476]
[fv-az1426-552:06154] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe7e3e287f3]
[fv-az1426-552:06154] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe7e42a2b9e]
[fv-az1426-552:06154] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe7e42ae20c]
[fv-az1426-552:06154] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe7e42ae277]
[fv-az1426-552:06154] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe7e42ae52b]
[fv-az1426-552:06154] [ 8] plumed(+0x12f48)[0x55d9277c4f48]
[fv-az1426-552:06154] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe7e3e29d90]
[fv-az1426-552:06154] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe7e3e29e40]
[fv-az1426-552:06154] [11] plumed(+0x131e5)[0x55d9277c51e5]
[fv-az1426-552:06154] *** End of error message ***
</pre>
{% endraw %}
