Stderr for source:  Steinhardt.md_working_17.dat   
Download: [zipped raw stdout](Steinhardt.md_working_17.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_17.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1535-978:70503] *** Process received signal ***
[fv-az1535-978:70503] Signal: Aborted (6)
[fv-az1535-978:70503] Signal code:  (-6)
[fv-az1535-978:70503] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fce38642520]
[fv-az1535-978:70503] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fce386969fc]
[fv-az1535-978:70503] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fce38642476]
[fv-az1535-978:70503] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fce386287f3]
[fv-az1535-978:70503] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fce38aa2b9e]
[fv-az1535-978:70503] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fce38aae20c]
[fv-az1535-978:70503] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fce38aae277]
[fv-az1535-978:70503] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fce38aae52b]
[fv-az1535-978:70503] [ 8] plumed(+0x12f48)[0x55acbe79ef48]
[fv-az1535-978:70503] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fce38629d90]
[fv-az1535-978:70503] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fce38629e40]
[fv-az1535-978:70503] [11] plumed(+0x131e5)[0x55acbe79f1e5]
[fv-az1535-978:70503] *** End of error message ***
</pre>
{% endraw %}
