Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az1429-301:04338] *** Process received signal ***
[fv-az1429-301:04338] Signal: Aborted (6)
[fv-az1429-301:04338] Signal code:  (-6)
[fv-az1429-301:04338] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4ffaa42520]
[fv-az1429-301:04338] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4ffaa969fc]
[fv-az1429-301:04338] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4ffaa42476]
[fv-az1429-301:04338] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4ffaa287f3]
[fv-az1429-301:04338] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4ffaea2b9e]
[fv-az1429-301:04338] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4ffaeae20c]
[fv-az1429-301:04338] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4ffaeae277]
[fv-az1429-301:04338] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4ffaeae52b]
[fv-az1429-301:04338] [ 8] plumed(+0x12f48)[0x5644e4e5af48]
[fv-az1429-301:04338] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4ffaa29d90]
[fv-az1429-301:04338] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4ffaa29e40]
[fv-az1429-301:04338] [11] plumed(+0x131e5)[0x5644e4e5b1e5]
[fv-az1429-301:04338] *** End of error message ***
</pre>
{% endraw %}
