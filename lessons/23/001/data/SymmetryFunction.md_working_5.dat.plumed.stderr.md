Stderr for source:  SymmetryFunction.md_working_5.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1426-552:05798] *** Process received signal ***
[fv-az1426-552:05798] Signal: Aborted (6)
[fv-az1426-552:05798] Signal code:  (-6)
[fv-az1426-552:05798] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7efc2e642520]
[fv-az1426-552:05798] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7efc2e6969fc]
[fv-az1426-552:05798] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7efc2e642476]
[fv-az1426-552:05798] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7efc2e6287f3]
[fv-az1426-552:05798] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7efc2eaa2b9e]
[fv-az1426-552:05798] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7efc2eaae20c]
[fv-az1426-552:05798] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7efc2eaae277]
[fv-az1426-552:05798] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7efc2eaae52b]
[fv-az1426-552:05798] [ 8] plumed(+0x12f48)[0x55ce07f14f48]
[fv-az1426-552:05798] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7efc2e629d90]
[fv-az1426-552:05798] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7efc2e629e40]
[fv-az1426-552:05798] [11] plumed(+0x131e5)[0x55ce07f151e5]
[fv-az1426-552:05798] *** End of error message ***
</pre>
{% endraw %}
