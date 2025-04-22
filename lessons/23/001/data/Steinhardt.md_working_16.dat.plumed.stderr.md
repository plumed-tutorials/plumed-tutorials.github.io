Stderr for source:  Steinhardt.md_working_16.dat   
Download: [zipped raw stdout](Steinhardt.md_working_16.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_16.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06774] *** Process received signal ***
[fv-az1315-757:06774] Signal: Aborted (6)
[fv-az1315-757:06774] Signal code:  (-6)
[fv-az1315-757:06774] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7eff6ba45330]
[fv-az1315-757:06774] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7eff6ba9eb2c]
[fv-az1315-757:06774] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7eff6ba4527e]
[fv-az1315-757:06774] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7eff6ba288ff]
[fv-az1315-757:06774] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7eff6bea5ff5]
[fv-az1315-757:06774] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7eff6bebb0da]
[fv-az1315-757:06774] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7eff6bea5a55]
[fv-az1315-757:06774] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7eff6bea5a6f]
[fv-az1315-757:06774] [ 8] plumed(+0x13209)[0x55ae739bc209]
[fv-az1315-757:06774] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7eff6ba2a1ca]
[fv-az1315-757:06774] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7eff6ba2a28b]
[fv-az1315-757:06774] [11] plumed(+0x134a5)[0x55ae739bc4a5]
[fv-az1315-757:06774] *** End of error message ***
</pre>
{% endraw %}
