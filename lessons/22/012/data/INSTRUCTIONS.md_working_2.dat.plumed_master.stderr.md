Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label @s9 : keyword SIGMA could not be read correctly
[fv-az1429-301:04299] *** Process received signal ***
[fv-az1429-301:04299] Signal: Aborted (6)
[fv-az1429-301:04299] Signal code:  (-6)
[fv-az1429-301:04299] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb7d2642520]
[fv-az1429-301:04299] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb7d26969fc]
[fv-az1429-301:04299] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb7d2642476]
[fv-az1429-301:04299] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb7d26287f3]
[fv-az1429-301:04299] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb7d2aa2b9e]
[fv-az1429-301:04299] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb7d2aae20c]
[fv-az1429-301:04299] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb7d2aae277]
[fv-az1429-301:04299] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb7d2aae52b]
[fv-az1429-301:04299] [ 8] plumed_master(+0x14254)[0x562bf63e1254]
[fv-az1429-301:04299] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb7d2629d90]
[fv-az1429-301:04299] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb7d2629e40]
[fv-az1429-301:04299] [11] plumed_master(+0x14eb5)[0x562bf63e1eb5]
[fv-az1429-301:04299] *** End of error message ***
</pre>
{% endraw %}
