Stderr for source:  Steinhardt.md_working_1.dat   
Download: [zipped raw stdout](Steinhardt.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1426-552:04985] *** Process received signal ***
[fv-az1426-552:04985] Signal: Aborted (6)
[fv-az1426-552:04985] Signal code:  (-6)
[fv-az1426-552:04985] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f812e842520]
[fv-az1426-552:04985] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f812e8969fc]
[fv-az1426-552:04985] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f812e842476]
[fv-az1426-552:04985] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f812e8287f3]
[fv-az1426-552:04985] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f812eca2b9e]
[fv-az1426-552:04985] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f812ecae20c]
[fv-az1426-552:04985] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f812ecae277]
[fv-az1426-552:04985] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f812ecae52b]
[fv-az1426-552:04985] [ 8] plumed(+0x12f48)[0x5559938a6f48]
[fv-az1426-552:04985] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f812e829d90]
[fv-az1426-552:04985] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f812e829e40]
[fv-az1426-552:04985] [11] plumed(+0x131e5)[0x5559938a71e5]
[fv-az1426-552:04985] *** End of error message ***
</pre>
{% endraw %}
