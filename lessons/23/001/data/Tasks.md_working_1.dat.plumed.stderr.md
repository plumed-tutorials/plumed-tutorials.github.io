Stderr for source:  Tasks.md_working_1.dat   
Download: [zipped raw stdout](Tasks.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1755-505:05929] *** Process received signal ***
[fv-az1755-505:05929] Signal: Aborted (6)
[fv-az1755-505:05929] Signal code:  (-6)
[fv-az1755-505:05929] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbffb045330]
[fv-az1755-505:05929] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbffb09eb2c]
[fv-az1755-505:05929] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbffb04527e]
[fv-az1755-505:05929] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbffb0288ff]
[fv-az1755-505:05929] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbffb4a5ff5]
[fv-az1755-505:05929] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbffb4bb0da]
[fv-az1755-505:05929] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbffb4a5a55]
[fv-az1755-505:05929] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbffb4a5a6f]
[fv-az1755-505:05929] [ 8] plumed(+0x13209)[0x56475049a209]
[fv-az1755-505:05929] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbffb02a1ca]
[fv-az1755-505:05929] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbffb02a28b]
[fv-az1755-505:05929] [11] plumed(+0x134a5)[0x56475049a4a5]
[fv-az1755-505:05929] *** End of error message ***
</pre>
{% endraw %}
