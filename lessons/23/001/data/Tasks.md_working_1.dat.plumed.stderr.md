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
[fv-az1315-757:06016] *** Process received signal ***
[fv-az1315-757:06016] Signal: Aborted (6)
[fv-az1315-757:06016] Signal code:  (-6)
[fv-az1315-757:06016] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe60fc45330]
[fv-az1315-757:06016] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe60fc9eb2c]
[fv-az1315-757:06016] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe60fc4527e]
[fv-az1315-757:06016] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe60fc288ff]
[fv-az1315-757:06016] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe6100a5ff5]
[fv-az1315-757:06016] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe6100bb0da]
[fv-az1315-757:06016] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe6100a5a55]
[fv-az1315-757:06016] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe6100a5a6f]
[fv-az1315-757:06016] [ 8] plumed(+0x13209)[0x55c61deea209]
[fv-az1315-757:06016] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe60fc2a1ca]
[fv-az1315-757:06016] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe60fc2a28b]
[fv-az1315-757:06016] [11] plumed(+0x134a5)[0x55c61deea4a5]
[fv-az1315-757:06016] *** End of error message ***
</pre>
{% endraw %}
