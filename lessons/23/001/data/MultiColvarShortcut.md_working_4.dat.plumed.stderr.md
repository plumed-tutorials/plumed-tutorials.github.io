Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1535-978:69644] *** Process received signal ***
[fv-az1535-978:69644] Signal: Aborted (6)
[fv-az1535-978:69644] Signal code:  (-6)
[fv-az1535-978:69644] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc522442520]
[fv-az1535-978:69644] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc5224969fc]
[fv-az1535-978:69644] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc522442476]
[fv-az1535-978:69644] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc5224287f3]
[fv-az1535-978:69644] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc5228a2b9e]
[fv-az1535-978:69644] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc5228ae20c]
[fv-az1535-978:69644] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc5228ae277]
[fv-az1535-978:69644] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc5228ae52b]
[fv-az1535-978:69644] [ 8] plumed(+0x12f48)[0x55a18385ef48]
[fv-az1535-978:69644] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc522429d90]
[fv-az1535-978:69644] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc522429e40]
[fv-az1535-978:69644] [11] plumed(+0x131e5)[0x55a18385f1e5]
[fv-az1535-978:69644] *** End of error message ***
</pre>
{% endraw %}
