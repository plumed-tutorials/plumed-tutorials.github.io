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
[fv-az573-691:04475] *** Process received signal ***
[fv-az573-691:04475] Signal: Aborted (6)
[fv-az573-691:04475] Signal code:  (-6)
[fv-az573-691:04475] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa09ec42520]
[fv-az573-691:04475] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa09ec969fc]
[fv-az573-691:04475] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa09ec42476]
[fv-az573-691:04475] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa09ec287f3]
[fv-az573-691:04475] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa09f0a2b9e]
[fv-az573-691:04475] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa09f0ae20c]
[fv-az573-691:04475] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa09f0ae277]
[fv-az573-691:04475] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa09f0ae52b]
[fv-az573-691:04475] [ 8] plumed(+0x12f48)[0x56497ed19f48]
[fv-az573-691:04475] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa09ec29d90]
[fv-az573-691:04475] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa09ec29e40]
[fv-az573-691:04475] [11] plumed(+0x131e5)[0x56497ed1a1e5]
[fv-az573-691:04475] *** End of error message ***
</pre>
{% endraw %}
