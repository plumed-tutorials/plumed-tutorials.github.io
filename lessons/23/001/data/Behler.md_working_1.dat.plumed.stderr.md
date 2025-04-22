Stderr for source:  Behler.md_working_1.dat   
Download: [zipped raw stdout](Behler.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06996] *** Process received signal ***
[fv-az1315-757:06996] Signal: Aborted (6)
[fv-az1315-757:06996] Signal code:  (-6)
[fv-az1315-757:06996] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9839245330]
[fv-az1315-757:06996] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f983929eb2c]
[fv-az1315-757:06996] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f983924527e]
[fv-az1315-757:06996] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f98392288ff]
[fv-az1315-757:06996] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f98396a5ff5]
[fv-az1315-757:06996] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f98396bb0da]
[fv-az1315-757:06996] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f98396a5a55]
[fv-az1315-757:06996] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f98396a5a6f]
[fv-az1315-757:06996] [ 8] plumed(+0x13209)[0x55a8e237c209]
[fv-az1315-757:06996] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f983922a1ca]
[fv-az1315-757:06996] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f983922a28b]
[fv-az1315-757:06996] [11] plumed(+0x134a5)[0x55a8e237c4a5]
[fv-az1315-757:06996] *** End of error message ***
</pre>
{% endraw %}
