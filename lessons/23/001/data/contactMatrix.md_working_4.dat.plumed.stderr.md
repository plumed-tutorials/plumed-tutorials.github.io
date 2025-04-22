Stderr for source:  contactMatrix.md_working_4.dat   
Download: [zipped raw stdout](contactMatrix.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1315-757:05824] *** Process received signal ***
[fv-az1315-757:05824] Signal: Aborted (6)
[fv-az1315-757:05824] Signal code:  (-6)
[fv-az1315-757:05824] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcd98a45330]
[fv-az1315-757:05824] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcd98a9eb2c]
[fv-az1315-757:05824] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcd98a4527e]
[fv-az1315-757:05824] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcd98a288ff]
[fv-az1315-757:05824] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcd98ea5ff5]
[fv-az1315-757:05824] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcd98ebb0da]
[fv-az1315-757:05824] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcd98ea5a55]
[fv-az1315-757:05824] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcd98ea5a6f]
[fv-az1315-757:05824] [ 8] plumed(+0x13209)[0x55e08c0ed209]
[fv-az1315-757:05824] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcd98a2a1ca]
[fv-az1315-757:05824] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcd98a2a28b]
[fv-az1315-757:05824] [11] plumed(+0x134a5)[0x55e08c0ed4a5]
[fv-az1315-757:05824] *** End of error message ***
</pre>
{% endraw %}
