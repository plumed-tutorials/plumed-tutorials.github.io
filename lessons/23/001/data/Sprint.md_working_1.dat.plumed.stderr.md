Stderr for source:  Sprint.md_working_1.dat   
Download: [zipped raw stdout](Sprint.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action SPRINT with label s1 : keyword MATRIX is compulsory for this action
[fv-az1426-552:04912] *** Process received signal ***
[fv-az1426-552:04912] Signal: Aborted (6)
[fv-az1426-552:04912] Signal code:  (-6)
[fv-az1426-552:04912] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f73e3442520]
[fv-az1426-552:04912] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f73e34969fc]
[fv-az1426-552:04912] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f73e3442476]
[fv-az1426-552:04912] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f73e34287f3]
[fv-az1426-552:04912] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f73e38a2b9e]
[fv-az1426-552:04912] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f73e38ae20c]
[fv-az1426-552:04912] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f73e38ae277]
[fv-az1426-552:04912] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f73e38ae52b]
[fv-az1426-552:04912] [ 8] plumed(+0x12f48)[0x560d2870cf48]
[fv-az1426-552:04912] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f73e3429d90]
[fv-az1426-552:04912] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f73e3429e40]
[fv-az1426-552:04912] [11] plumed(+0x131e5)[0x560d2870d1e5]
[fv-az1426-552:04912] *** End of error message ***
</pre>
{% endraw %}
