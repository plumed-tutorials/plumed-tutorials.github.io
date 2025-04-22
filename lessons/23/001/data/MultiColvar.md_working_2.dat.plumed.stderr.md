Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1315-757:05451] *** Process received signal ***
[fv-az1315-757:05451] Signal: Aborted (6)
[fv-az1315-757:05451] Signal code:  (-6)
[fv-az1315-757:05451] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa6ffa45330]
[fv-az1315-757:05451] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa6ffa9eb2c]
[fv-az1315-757:05451] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa6ffa4527e]
[fv-az1315-757:05451] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa6ffa288ff]
[fv-az1315-757:05451] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa6ffea5ff5]
[fv-az1315-757:05451] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa6ffebb0da]
[fv-az1315-757:05451] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa6ffea5a55]
[fv-az1315-757:05451] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa6ffea5a6f]
[fv-az1315-757:05451] [ 8] plumed(+0x13209)[0x56228e46e209]
[fv-az1315-757:05451] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa6ffa2a1ca]
[fv-az1315-757:05451] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa6ffa2a28b]
[fv-az1315-757:05451] [11] plumed(+0x134a5)[0x56228e46e4a5]
[fv-az1315-757:05451] *** End of error message ***
</pre>
{% endraw %}
