Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[fv-az1535-978:70346] *** Process received signal ***
[fv-az1535-978:70346] Signal: Aborted (6)
[fv-az1535-978:70346] Signal code:  (-6)
[fv-az1535-978:70346] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1a3ea42520]
[fv-az1535-978:70346] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1a3ea969fc]
[fv-az1535-978:70346] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1a3ea42476]
[fv-az1535-978:70346] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1a3ea287f3]
[fv-az1535-978:70346] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1a3eea2b9e]
[fv-az1535-978:70346] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1a3eeae20c]
[fv-az1535-978:70346] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1a3eeae277]
[fv-az1535-978:70346] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1a3eeae52b]
[fv-az1535-978:70346] [ 8] plumed(+0x12f48)[0x55e6ab6d5f48]
[fv-az1535-978:70346] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1a3ea29d90]
[fv-az1535-978:70346] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1a3ea29e40]
[fv-az1535-978:70346] [11] plumed(+0x131e5)[0x55e6ab6d61e5]
[fv-az1535-978:70346] *** End of error message ***
</pre>
{% endraw %}
