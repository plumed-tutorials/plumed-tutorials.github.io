Stderr for source:  Behler.md_working_6.dat   
Download: [zipped raw stdout](Behler.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:07154] *** Process received signal ***
[fv-az1315-757:07154] Signal: Aborted (6)
[fv-az1315-757:07154] Signal code:  (-6)
[fv-az1315-757:07154] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3752845330]
[fv-az1315-757:07154] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f375289eb2c]
[fv-az1315-757:07154] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f375284527e]
[fv-az1315-757:07154] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f37528288ff]
[fv-az1315-757:07154] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3752ca5ff5]
[fv-az1315-757:07154] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3752cbb0da]
[fv-az1315-757:07154] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3752ca5a55]
[fv-az1315-757:07154] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3752ca5a6f]
[fv-az1315-757:07154] [ 8] plumed(+0x13209)[0x563a4a21e209]
[fv-az1315-757:07154] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f375282a1ca]
[fv-az1315-757:07154] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f375282a28b]
[fv-az1315-757:07154] [11] plumed(+0x134a5)[0x563a4a21e4a5]
[fv-az1315-757:07154] *** End of error message ***
</pre>
{% endraw %}
