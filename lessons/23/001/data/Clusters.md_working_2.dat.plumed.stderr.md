Stderr for source:  Clusters.md_working_2.dat   
Download: [zipped raw stdout](Clusters.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1426-552:06392] *** Process received signal ***
[fv-az1426-552:06392] Signal: Aborted (6)
[fv-az1426-552:06392] Signal code:  (-6)
[fv-az1426-552:06392] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe05f842520]
[fv-az1426-552:06392] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe05f8969fc]
[fv-az1426-552:06392] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe05f842476]
[fv-az1426-552:06392] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe05f8287f3]
[fv-az1426-552:06392] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe05fca2b9e]
[fv-az1426-552:06392] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe05fcae20c]
[fv-az1426-552:06392] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe05fcae277]
[fv-az1426-552:06392] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe05fcae52b]
[fv-az1426-552:06392] [ 8] plumed(+0x12f48)[0x55ab11a6ef48]
[fv-az1426-552:06392] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe05f829d90]
[fv-az1426-552:06392] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe05f829e40]
[fv-az1426-552:06392] [11] plumed(+0x131e5)[0x55ab11a6f1e5]
[fv-az1426-552:06392] *** End of error message ***
</pre>
{% endraw %}
