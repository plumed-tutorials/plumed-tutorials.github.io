Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[fv-az573-691:04429] *** Process received signal ***
[fv-az573-691:04429] Signal: Aborted (6)
[fv-az573-691:04429] Signal code:  (-6)
[fv-az573-691:04429] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe288442520]
[fv-az573-691:04429] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe2884969fc]
[fv-az573-691:04429] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe288442476]
[fv-az573-691:04429] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe2884287f3]
[fv-az573-691:04429] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe2888a2b9e]
[fv-az573-691:04429] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe2888ae20c]
[fv-az573-691:04429] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe2888ae277]
[fv-az573-691:04429] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe2888ae52b]
[fv-az573-691:04429] [ 8] plumed(+0x12f48)[0x56034bc14f48]
[fv-az573-691:04429] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe288429d90]
[fv-az573-691:04429] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe288429e40]
[fv-az573-691:04429] [11] plumed(+0x131e5)[0x56034bc151e5]
[fv-az573-691:04429] *** End of error message ***
</pre>
{% endraw %}
