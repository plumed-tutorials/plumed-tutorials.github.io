Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az1530-405:69764] *** Process received signal ***
[fv-az1530-405:69764] Signal: Aborted (6)
[fv-az1530-405:69764] Signal code:  (-6)
[fv-az1530-405:69764] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa6a4642520]
[fv-az1530-405:69764] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa6a46969fc]
[fv-az1530-405:69764] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa6a4642476]
[fv-az1530-405:69764] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa6a46287f3]
[fv-az1530-405:69764] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa6a4aa2b9e]
[fv-az1530-405:69764] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa6a4aae20c]
[fv-az1530-405:69764] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa6a4aae277]
[fv-az1530-405:69764] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa6a4aae52b]
[fv-az1530-405:69764] [ 8] plumed(+0x12f48)[0x564e1a048f48]
[fv-az1530-405:69764] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa6a4629d90]
[fv-az1530-405:69764] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa6a4629e40]
[fv-az1530-405:69764] [11] plumed(+0x131e5)[0x564e1a0491e5]
[fv-az1530-405:69764] *** End of error message ***
</pre>
{% endraw %}
