Stderr for source:  Steinhardt.md_working_18.dat   
Download: [zipped raw stdout](Steinhardt.md_working_18.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_18.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1535-978:70525] *** Process received signal ***
[fv-az1535-978:70525] Signal: Aborted (6)
[fv-az1535-978:70525] Signal code:  (-6)
[fv-az1535-978:70525] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb540642520]
[fv-az1535-978:70525] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb5406969fc]
[fv-az1535-978:70525] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb540642476]
[fv-az1535-978:70525] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb5406287f3]
[fv-az1535-978:70525] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb540aa2b9e]
[fv-az1535-978:70525] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb540aae20c]
[fv-az1535-978:70525] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb540aae277]
[fv-az1535-978:70525] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb540aae52b]
[fv-az1535-978:70525] [ 8] plumed(+0x12f48)[0x561be98edf48]
[fv-az1535-978:70525] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb540629d90]
[fv-az1535-978:70525] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb540629e40]
[fv-az1535-978:70525] [11] plumed(+0x131e5)[0x561be98ee1e5]
[fv-az1535-978:70525] *** End of error message ***
</pre>
{% endraw %}
