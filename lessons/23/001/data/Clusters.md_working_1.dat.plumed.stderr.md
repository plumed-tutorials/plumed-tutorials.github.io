Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1535-978:71528] *** Process received signal ***
[fv-az1535-978:71528] Signal: Aborted (6)
[fv-az1535-978:71528] Signal code:  (-6)
[fv-az1535-978:71528] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f5c64442520]
[fv-az1535-978:71528] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f5c644969fc]
[fv-az1535-978:71528] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f5c64442476]
[fv-az1535-978:71528] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f5c644287f3]
[fv-az1535-978:71528] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f5c648a2b9e]
[fv-az1535-978:71528] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f5c648ae20c]
[fv-az1535-978:71528] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f5c648ae277]
[fv-az1535-978:71528] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f5c648ae52b]
[fv-az1535-978:71528] [ 8] plumed(+0x12f48)[0x558d30046f48]
[fv-az1535-978:71528] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f5c64429d90]
[fv-az1535-978:71528] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f5c64429e40]
[fv-az1535-978:71528] [11] plumed(+0x131e5)[0x558d300471e5]
[fv-az1535-978:71528] *** End of error message ***
</pre>
{% endraw %}
