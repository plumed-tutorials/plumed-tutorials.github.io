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
[fv-az1426-552:05076] *** Process received signal ***
[fv-az1426-552:05076] Signal: Aborted (6)
[fv-az1426-552:05076] Signal code:  (-6)
[fv-az1426-552:05076] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f514a442520]
[fv-az1426-552:05076] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f514a4969fc]
[fv-az1426-552:05076] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f514a442476]
[fv-az1426-552:05076] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f514a4287f3]
[fv-az1426-552:05076] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f514a8a2b9e]
[fv-az1426-552:05076] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f514a8ae20c]
[fv-az1426-552:05076] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f514a8ae277]
[fv-az1426-552:05076] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f514a8ae52b]
[fv-az1426-552:05076] [ 8] plumed(+0x12f48)[0x5642c5c4bf48]
[fv-az1426-552:05076] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f514a429d90]
[fv-az1426-552:05076] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f514a429e40]
[fv-az1426-552:05076] [11] plumed(+0x131e5)[0x5642c5c4c1e5]
[fv-az1426-552:05076] *** End of error message ***
</pre>
{% endraw %}
