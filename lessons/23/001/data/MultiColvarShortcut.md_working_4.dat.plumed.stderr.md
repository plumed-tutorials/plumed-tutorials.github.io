Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1315-757:05648] *** Process received signal ***
[fv-az1315-757:05648] Signal: Aborted (6)
[fv-az1315-757:05648] Signal code:  (-6)
[fv-az1315-757:05648] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1ca1c45330]
[fv-az1315-757:05648] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1ca1c9eb2c]
[fv-az1315-757:05648] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1ca1c4527e]
[fv-az1315-757:05648] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1ca1c288ff]
[fv-az1315-757:05648] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1ca20a5ff5]
[fv-az1315-757:05648] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1ca20bb0da]
[fv-az1315-757:05648] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1ca20a5a55]
[fv-az1315-757:05648] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1ca20a5a6f]
[fv-az1315-757:05648] [ 8] plumed(+0x13209)[0x560f67aa2209]
[fv-az1315-757:05648] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1ca1c2a1ca]
[fv-az1315-757:05648] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1ca1c2a28b]
[fv-az1315-757:05648] [11] plumed(+0x134a5)[0x560f67aa24a5]
[fv-az1315-757:05648] *** End of error message ***
</pre>
{% endraw %}
