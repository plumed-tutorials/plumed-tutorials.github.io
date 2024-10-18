Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1535-978:71573] *** Process received signal ***
[fv-az1535-978:71573] Signal: Aborted (6)
[fv-az1535-978:71573] Signal code:  (-6)
[fv-az1535-978:71573] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fafd3242520]
[fv-az1535-978:71573] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fafd32969fc]
[fv-az1535-978:71573] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fafd3242476]
[fv-az1535-978:71573] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fafd32287f3]
[fv-az1535-978:71573] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fafd36a2b9e]
[fv-az1535-978:71573] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fafd36ae20c]
[fv-az1535-978:71573] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fafd36ae277]
[fv-az1535-978:71573] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fafd36ae52b]
[fv-az1535-978:71573] [ 8] plumed(+0x12f48)[0x5572dfc4af48]
[fv-az1535-978:71573] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fafd3229d90]
[fv-az1535-978:71573] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fafd3229e40]
[fv-az1535-978:71573] [11] plumed(+0x131e5)[0x5572dfc4b1e5]
[fv-az1535-978:71573] *** End of error message ***
</pre>
{% endraw %}
