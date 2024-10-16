Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[fv-az1426-552:04934] *** Process received signal ***
[fv-az1426-552:04934] Signal: Aborted (6)
[fv-az1426-552:04934] Signal code:  (-6)
[fv-az1426-552:04934] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1042242520]
[fv-az1426-552:04934] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f10422969fc]
[fv-az1426-552:04934] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1042242476]
[fv-az1426-552:04934] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f10422287f3]
[fv-az1426-552:04934] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f10426a2b9e]
[fv-az1426-552:04934] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f10426ae20c]
[fv-az1426-552:04934] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f10426ae277]
[fv-az1426-552:04934] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f10426ae52b]
[fv-az1426-552:04934] [ 8] plumed(+0x12f48)[0x55da48f5ff48]
[fv-az1426-552:04934] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1042229d90]
[fv-az1426-552:04934] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1042229e40]
[fv-az1426-552:04934] [11] plumed(+0x131e5)[0x55da48f601e5]
[fv-az1426-552:04934] *** End of error message ***
</pre>
{% endraw %}
