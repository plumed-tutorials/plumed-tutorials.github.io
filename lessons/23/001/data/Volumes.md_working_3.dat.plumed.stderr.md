Stderr for source:  Volumes.md_working_3.dat   
Download: [zipped raw stdout](Volumes.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:07254] *** Process received signal ***
[fv-az1315-757:07254] Signal: Aborted (6)
[fv-az1315-757:07254] Signal code:  (-6)
[fv-az1315-757:07254] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4e6a845330]
[fv-az1315-757:07254] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4e6a89eb2c]
[fv-az1315-757:07254] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4e6a84527e]
[fv-az1315-757:07254] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4e6a8288ff]
[fv-az1315-757:07254] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4e6aca5ff5]
[fv-az1315-757:07254] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4e6acbb0da]
[fv-az1315-757:07254] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4e6aca5a55]
[fv-az1315-757:07254] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4e6aca5a6f]
[fv-az1315-757:07254] [ 8] plumed(+0x13209)[0x55f453cf0209]
[fv-az1315-757:07254] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4e6a82a1ca]
[fv-az1315-757:07254] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4e6a82a28b]
[fv-az1315-757:07254] [11] plumed(+0x134a5)[0x55f453cf04a5]
[fv-az1315-757:07254] *** End of error message ***
</pre>
{% endraw %}
