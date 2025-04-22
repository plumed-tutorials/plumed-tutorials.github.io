Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1315-757:08232] *** Process received signal ***
[fv-az1315-757:08232] Signal: Aborted (6)
[fv-az1315-757:08232] Signal code:  (-6)
[fv-az1315-757:08232] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8393445330]
[fv-az1315-757:08232] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f839349eb2c]
[fv-az1315-757:08232] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f839344527e]
[fv-az1315-757:08232] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f83934288ff]
[fv-az1315-757:08232] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f83938a5ff5]
[fv-az1315-757:08232] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f83938bb0da]
[fv-az1315-757:08232] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f83938a5a55]
[fv-az1315-757:08232] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f83938a5a6f]
[fv-az1315-757:08232] [ 8] plumed(+0x13209)[0x5646cdad4209]
[fv-az1315-757:08232] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f839342a1ca]
[fv-az1315-757:08232] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f839342a28b]
[fv-az1315-757:08232] [11] plumed(+0x134a5)[0x5646cdad44a5]
[fv-az1315-757:08232] *** End of error message ***
</pre>
{% endraw %}
