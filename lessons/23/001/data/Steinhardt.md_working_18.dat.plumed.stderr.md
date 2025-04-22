Stderr for source:  Steinhardt.md_working_18.dat   
Download: [zipped raw stdout](Steinhardt.md_working_18.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_18.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06836] *** Process received signal ***
[fv-az1315-757:06836] Signal: Aborted (6)
[fv-az1315-757:06836] Signal code:  (-6)
[fv-az1315-757:06836] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4ddaa45330]
[fv-az1315-757:06836] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4ddaa9eb2c]
[fv-az1315-757:06836] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4ddaa4527e]
[fv-az1315-757:06836] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4ddaa288ff]
[fv-az1315-757:06836] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4ddaea5ff5]
[fv-az1315-757:06836] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4ddaebb0da]
[fv-az1315-757:06836] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4ddaea5a55]
[fv-az1315-757:06836] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4ddaea5a6f]
[fv-az1315-757:06836] [ 8] plumed(+0x13209)[0x55a2914d3209]
[fv-az1315-757:06836] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4ddaa2a1ca]
[fv-az1315-757:06836] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4ddaa2a28b]
[fv-az1315-757:06836] [11] plumed(+0x134a5)[0x55a2914d34a5]
[fv-az1315-757:06836] *** End of error message ***
</pre>
{% endraw %}
