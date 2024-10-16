Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az573-691:04483] *** Process received signal ***
[fv-az573-691:04483] Signal: Aborted (6)
[fv-az573-691:04483] Signal code:  (-6)
[fv-az573-691:04483] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe769842520]
[fv-az573-691:04483] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe7698969fc]
[fv-az573-691:04483] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe769842476]
[fv-az573-691:04483] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe7698287f3]
[fv-az573-691:04483] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe769ca2b9e]
[fv-az573-691:04483] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe769cae20c]
[fv-az573-691:04483] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe769cae277]
[fv-az573-691:04483] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe769cae52b]
[fv-az573-691:04483] [ 8] plumed_master(+0x14254)[0x564543052254]
[fv-az573-691:04483] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe769829d90]
[fv-az573-691:04483] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe769829e40]
[fv-az573-691:04483] [11] plumed_master(+0x14eb5)[0x564543052eb5]
[fv-az573-691:04483] *** End of error message ***
</pre>
{% endraw %}
