Stderr for source:  Steinhardt.md_working_5.dat   
Download: [zipped raw stdout](Steinhardt.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action PRINT with label @1 : action q4 has no component named q4 (hint! the components in this actions are: )
[fv-az1020-777:04924] *** Process received signal ***
[fv-az1020-777:04924] Signal: Aborted (6)
[fv-az1020-777:04924] Signal code:  (-6)
[fv-az1020-777:04924] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f91db642520]
[fv-az1020-777:04924] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f91db6969fc]
[fv-az1020-777:04924] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f91db642476]
[fv-az1020-777:04924] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f91db6287f3]
[fv-az1020-777:04924] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f91dbaa2b9e]
[fv-az1020-777:04924] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f91dbaae20c]
[fv-az1020-777:04924] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f91dbaae277]
[fv-az1020-777:04924] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f91dbaae52b]
[fv-az1020-777:04924] [ 8] plumed(+0x12f48)[0x5605e691df48]
[fv-az1020-777:04924] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f91db629d90]
[fv-az1020-777:04924] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f91db629e40]
[fv-az1020-777:04924] [11] plumed(+0x131e5)[0x5605e691e1e5]
[fv-az1020-777:04924] *** End of error message ***
</pre>
{% endraw %}
