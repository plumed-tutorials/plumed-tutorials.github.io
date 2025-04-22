Stderr for source:  Steinhardt.md_working_15.dat   
Download: [zipped raw stdout](Steinhardt.md_working_15.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_15.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06743] *** Process received signal ***
[fv-az1315-757:06743] Signal: Aborted (6)
[fv-az1315-757:06743] Signal code:  (-6)
[fv-az1315-757:06743] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb0dcc45330]
[fv-az1315-757:06743] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb0dcc9eb2c]
[fv-az1315-757:06743] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb0dcc4527e]
[fv-az1315-757:06743] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb0dcc288ff]
[fv-az1315-757:06743] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb0dd0a5ff5]
[fv-az1315-757:06743] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb0dd0bb0da]
[fv-az1315-757:06743] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb0dd0a5a55]
[fv-az1315-757:06743] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb0dd0a5a6f]
[fv-az1315-757:06743] [ 8] plumed(+0x13209)[0x55994a3b1209]
[fv-az1315-757:06743] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb0dcc2a1ca]
[fv-az1315-757:06743] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb0dcc2a28b]
[fv-az1315-757:06743] [11] plumed(+0x134a5)[0x55994a3b14a5]
[fv-az1315-757:06743] *** End of error message ***
</pre>
{% endraw %}
