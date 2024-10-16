Stderr for source:  Volumes.md_working_2.dat   
Download: [zipped raw stdout](Volumes.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[fv-az1426-552:05589] *** Process received signal ***
[fv-az1426-552:05589] Signal: Aborted (6)
[fv-az1426-552:05589] Signal code:  (-6)
[fv-az1426-552:05589] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd8d7242520]
[fv-az1426-552:05589] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd8d72969fc]
[fv-az1426-552:05589] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd8d7242476]
[fv-az1426-552:05589] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd8d72287f3]
[fv-az1426-552:05589] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd8d76a2b9e]
[fv-az1426-552:05589] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd8d76ae20c]
[fv-az1426-552:05589] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd8d76ae277]
[fv-az1426-552:05589] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd8d76ae52b]
[fv-az1426-552:05589] [ 8] plumed(+0x12f48)[0x557869b93f48]
[fv-az1426-552:05589] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd8d7229d90]
[fv-az1426-552:05589] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd8d7229e40]
[fv-az1426-552:05589] [11] plumed(+0x131e5)[0x557869b941e5]
[fv-az1426-552:05589] *** End of error message ***
</pre>
{% endraw %}
