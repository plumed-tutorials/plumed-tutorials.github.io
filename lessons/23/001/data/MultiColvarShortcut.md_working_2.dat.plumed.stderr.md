Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1315-757:05593] *** Process received signal ***
[fv-az1315-757:05593] Signal: Aborted (6)
[fv-az1315-757:05593] Signal code:  (-6)
[fv-az1315-757:05593] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8ef6845330]
[fv-az1315-757:05593] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8ef689eb2c]
[fv-az1315-757:05593] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8ef684527e]
[fv-az1315-757:05593] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8ef68288ff]
[fv-az1315-757:05593] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8ef6ca5ff5]
[fv-az1315-757:05593] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8ef6cbb0da]
[fv-az1315-757:05593] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8ef6ca5a55]
[fv-az1315-757:05593] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8ef6ca5a6f]
[fv-az1315-757:05593] [ 8] plumed(+0x13209)[0x55c7997ea209]
[fv-az1315-757:05593] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8ef682a1ca]
[fv-az1315-757:05593] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8ef682a28b]
[fv-az1315-757:05593] [11] plumed(+0x134a5)[0x55c7997ea4a5]
[fv-az1315-757:05593] *** End of error message ***
</pre>
{% endraw %}
