Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1020-199:04307] *** Process received signal ***
[fv-az1020-199:04307] Signal: Aborted (6)
[fv-az1020-199:04307] Signal code:  (-6)
[fv-az1020-199:04307] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f97a7842520]
[fv-az1020-199:04307] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f97a78969fc]
[fv-az1020-199:04307] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f97a7842476]
[fv-az1020-199:04307] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f97a78287f3]
[fv-az1020-199:04307] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f97a7ca2b9e]
[fv-az1020-199:04307] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f97a7cae20c]
[fv-az1020-199:04307] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f97a7cae277]
[fv-az1020-199:04307] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f97a7cae52b]
[fv-az1020-199:04307] [ 8] plumed(+0x12f48)[0x562cb96a9f48]
[fv-az1020-199:04307] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f97a7829d90]
[fv-az1020-199:04307] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f97a7829e40]
[fv-az1020-199:04307] [11] plumed(+0x131e5)[0x562cb96aa1e5]
[fv-az1020-199:04307] *** End of error message ***
</pre>
{% endraw %}
