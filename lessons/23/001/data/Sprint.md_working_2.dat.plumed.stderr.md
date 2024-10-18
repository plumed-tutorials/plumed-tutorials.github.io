Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[fv-az1535-978:70093] *** Process received signal ***
[fv-az1535-978:70093] Signal: Aborted (6)
[fv-az1535-978:70093] Signal code:  (-6)
[fv-az1535-978:70093] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb2bb042520]
[fv-az1535-978:70093] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb2bb0969fc]
[fv-az1535-978:70093] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb2bb042476]
[fv-az1535-978:70093] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb2bb0287f3]
[fv-az1535-978:70093] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb2bb4a2b9e]
[fv-az1535-978:70093] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb2bb4ae20c]
[fv-az1535-978:70093] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb2bb4ae277]
[fv-az1535-978:70093] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb2bb4ae52b]
[fv-az1535-978:70093] [ 8] plumed(+0x12f48)[0x559778440f48]
[fv-az1535-978:70093] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb2bb029d90]
[fv-az1535-978:70093] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb2bb029e40]
[fv-az1535-978:70093] [11] plumed(+0x131e5)[0x5597784411e5]
[fv-az1535-978:70093] *** End of error message ***
</pre>
{% endraw %}
