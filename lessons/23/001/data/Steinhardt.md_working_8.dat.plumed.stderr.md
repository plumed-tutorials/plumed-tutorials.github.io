Stderr for source:  Steinhardt.md_working_8.dat   
Download: [zipped raw stdout](Steinhardt.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1535-978:70302] *** Process received signal ***
[fv-az1535-978:70302] Signal: Aborted (6)
[fv-az1535-978:70302] Signal code:  (-6)
[fv-az1535-978:70302] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f7236042520]
[fv-az1535-978:70302] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f72360969fc]
[fv-az1535-978:70302] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f7236042476]
[fv-az1535-978:70302] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f72360287f3]
[fv-az1535-978:70302] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f72364a2b9e]
[fv-az1535-978:70302] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f72364ae20c]
[fv-az1535-978:70302] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f72364ae277]
[fv-az1535-978:70302] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f72364ae52b]
[fv-az1535-978:70302] [ 8] plumed(+0x12f48)[0x55f2a3c92f48]
[fv-az1535-978:70302] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f7236029d90]
[fv-az1535-978:70302] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f7236029e40]
[fv-az1535-978:70302] [11] plumed(+0x131e5)[0x55f2a3c931e5]
[fv-az1535-978:70302] *** End of error message ***
</pre>
{% endraw %}
