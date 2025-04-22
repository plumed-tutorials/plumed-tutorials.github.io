Stderr for source:  Steinhardt.md_working_2.dat   
Download: [zipped raw stdout](Steinhardt.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1315-757:06327] *** Process received signal ***
[fv-az1315-757:06327] Signal: Aborted (6)
[fv-az1315-757:06327] Signal code:  (-6)
[fv-az1315-757:06327] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f31a4e45330]
[fv-az1315-757:06327] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f31a4e9eb2c]
[fv-az1315-757:06327] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f31a4e4527e]
[fv-az1315-757:06327] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f31a4e288ff]
[fv-az1315-757:06327] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f31a52a5ff5]
[fv-az1315-757:06327] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f31a52bb0da]
[fv-az1315-757:06327] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f31a52a5a55]
[fv-az1315-757:06327] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f31a52a5a6f]
[fv-az1315-757:06327] [ 8] plumed(+0x13209)[0x5596bce10209]
[fv-az1315-757:06327] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f31a4e2a1ca]
[fv-az1315-757:06327] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f31a4e2a28b]
[fv-az1315-757:06327] [11] plumed(+0x134a5)[0x5596bce104a5]
[fv-az1315-757:06327] *** End of error message ***
</pre>
{% endraw %}
