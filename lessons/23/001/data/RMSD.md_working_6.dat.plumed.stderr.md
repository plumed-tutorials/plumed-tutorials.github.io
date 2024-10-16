Stderr for source:  RMSD.md_working_6.dat   
Download: [zipped raw stdout](RMSD.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action RMSD with label rmsd : cannot understand the following words from the input line : DISPLACEMENT
[fv-az1426-552:06562] *** Process received signal ***
[fv-az1426-552:06562] Signal: Aborted (6)
[fv-az1426-552:06562] Signal code:  (-6)
[fv-az1426-552:06562] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f551d042520]
[fv-az1426-552:06562] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f551d0969fc]
[fv-az1426-552:06562] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f551d042476]
[fv-az1426-552:06562] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f551d0287f3]
[fv-az1426-552:06562] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f551d4a2b9e]
[fv-az1426-552:06562] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f551d4ae20c]
[fv-az1426-552:06562] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f551d4ae277]
[fv-az1426-552:06562] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f551d4ae52b]
[fv-az1426-552:06562] [ 8] plumed(+0x12f48)[0x55b1a356af48]
[fv-az1426-552:06562] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f551d029d90]
[fv-az1426-552:06562] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f551d029e40]
[fv-az1426-552:06562] [11] plumed(+0x131e5)[0x55b1a356b1e5]
[fv-az1426-552:06562] *** End of error message ***
</pre>
{% endraw %}
