Stderr for source:  Steinhardt.md_working_11.dat   
Download: [zipped raw stdout](Steinhardt.md_working_11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1535-978:70368] *** Process received signal ***
[fv-az1535-978:70368] Signal: Aborted (6)
[fv-az1535-978:70368] Signal code:  (-6)
[fv-az1535-978:70368] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f7c3e642520]
[fv-az1535-978:70368] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f7c3e6969fc]
[fv-az1535-978:70368] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f7c3e642476]
[fv-az1535-978:70368] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f7c3e6287f3]
[fv-az1535-978:70368] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f7c3eaa2b9e]
[fv-az1535-978:70368] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f7c3eaae20c]
[fv-az1535-978:70368] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f7c3eaae277]
[fv-az1535-978:70368] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f7c3eaae52b]
[fv-az1535-978:70368] [ 8] plumed(+0x12f48)[0x5608fc393f48]
[fv-az1535-978:70368] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f7c3e629d90]
[fv-az1535-978:70368] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f7c3e629e40]
[fv-az1535-978:70368] [11] plumed(+0x131e5)[0x5608fc3941e5]
[fv-az1535-978:70368] *** End of error message ***
</pre>
{% endraw %}
