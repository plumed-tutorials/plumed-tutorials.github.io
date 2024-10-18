Stderr for source:  Steinhardt.md_working_12.dat   
Download: [zipped raw stdout](Steinhardt.md_working_12.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_12.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1535-978:70392] *** Process received signal ***
[fv-az1535-978:70392] Signal: Aborted (6)
[fv-az1535-978:70392] Signal code:  (-6)
[fv-az1535-978:70392] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2062842520]
[fv-az1535-978:70392] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f20628969fc]
[fv-az1535-978:70392] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2062842476]
[fv-az1535-978:70392] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f20628287f3]
[fv-az1535-978:70392] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f2062ca2b9e]
[fv-az1535-978:70392] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f2062cae20c]
[fv-az1535-978:70392] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f2062cae277]
[fv-az1535-978:70392] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f2062cae52b]
[fv-az1535-978:70392] [ 8] plumed(+0x12f48)[0x55e42d9c9f48]
[fv-az1535-978:70392] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2062829d90]
[fv-az1535-978:70392] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2062829e40]
[fv-az1535-978:70392] [11] plumed(+0x131e5)[0x55e42d9ca1e5]
[fv-az1535-978:70392] *** End of error message ***
</pre>
{% endraw %}
