Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[fv-az1315-757:06233] *** Process received signal ***
[fv-az1315-757:06233] Signal: Aborted (6)
[fv-az1315-757:06233] Signal code:  (-6)
[fv-az1315-757:06233] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f11cda45330]
[fv-az1315-757:06233] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f11cda9eb2c]
[fv-az1315-757:06233] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f11cda4527e]
[fv-az1315-757:06233] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f11cda288ff]
[fv-az1315-757:06233] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f11cdea5ff5]
[fv-az1315-757:06233] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f11cdebb0da]
[fv-az1315-757:06233] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f11cdea5a55]
[fv-az1315-757:06233] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f11cdea5a6f]
[fv-az1315-757:06233] [ 8] plumed(+0x13209)[0x5555bc638209]
[fv-az1315-757:06233] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f11cda2a1ca]
[fv-az1315-757:06233] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f11cda2a28b]
[fv-az1315-757:06233] [11] plumed(+0x134a5)[0x5555bc6384a5]
[fv-az1315-757:06233] *** End of error message ***
</pre>
{% endraw %}
