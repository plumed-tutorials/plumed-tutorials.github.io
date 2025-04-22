Stderr for source:  Steinhardt.md_working_11.dat   
Download: [zipped raw stdout](Steinhardt.md_working_11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06614] *** Process received signal ***
[fv-az1315-757:06614] Signal: Aborted (6)
[fv-az1315-757:06614] Signal code:  (-6)
[fv-az1315-757:06614] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1681645330]
[fv-az1315-757:06614] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f168169eb2c]
[fv-az1315-757:06614] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f168164527e]
[fv-az1315-757:06614] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f16816288ff]
[fv-az1315-757:06614] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1681aa5ff5]
[fv-az1315-757:06614] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1681abb0da]
[fv-az1315-757:06614] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1681aa5a55]
[fv-az1315-757:06614] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1681aa5a6f]
[fv-az1315-757:06614] [ 8] plumed(+0x13209)[0x56385cfa6209]
[fv-az1315-757:06614] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f168162a1ca]
[fv-az1315-757:06614] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f168162a28b]
[fv-az1315-757:06614] [11] plumed(+0x134a5)[0x56385cfa64a5]
[fv-az1315-757:06614] *** End of error message ***
</pre>
{% endraw %}
