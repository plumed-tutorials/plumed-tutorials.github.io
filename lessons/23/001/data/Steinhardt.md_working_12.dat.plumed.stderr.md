Stderr for source:  Steinhardt.md_working_12.dat   
Download: [zipped raw stdout](Steinhardt.md_working_12.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_12.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1426-552:05234] *** Process received signal ***
[fv-az1426-552:05234] Signal: Aborted (6)
[fv-az1426-552:05234] Signal code:  (-6)
[fv-az1426-552:05234] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff84c842520]
[fv-az1426-552:05234] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff84c8969fc]
[fv-az1426-552:05234] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff84c842476]
[fv-az1426-552:05234] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff84c8287f3]
[fv-az1426-552:05234] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff84cca2b9e]
[fv-az1426-552:05234] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff84ccae20c]
[fv-az1426-552:05234] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff84ccae277]
[fv-az1426-552:05234] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff84ccae52b]
[fv-az1426-552:05234] [ 8] plumed(+0x12f48)[0x55a89ee22f48]
[fv-az1426-552:05234] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff84c829d90]
[fv-az1426-552:05234] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff84c829e40]
[fv-az1426-552:05234] [11] plumed(+0x131e5)[0x55a89ee231e5]
[fv-az1426-552:05234] *** End of error message ***
</pre>
{% endraw %}
