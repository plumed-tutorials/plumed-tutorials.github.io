Stderr for source:  Tasks.md_working_2.dat   
Download: [zipped raw stdout](Tasks.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1315-757:06060] *** Process received signal ***
[fv-az1315-757:06060] Signal: Aborted (6)
[fv-az1315-757:06060] Signal code:  (-6)
[fv-az1315-757:06060] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fda05645330]
[fv-az1315-757:06060] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fda0569eb2c]
[fv-az1315-757:06060] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fda0564527e]
[fv-az1315-757:06060] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fda056288ff]
[fv-az1315-757:06060] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fda05aa5ff5]
[fv-az1315-757:06060] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fda05abb0da]
[fv-az1315-757:06060] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fda05aa5a55]
[fv-az1315-757:06060] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fda05aa5a6f]
[fv-az1315-757:06060] [ 8] plumed(+0x13209)[0x56048dec1209]
[fv-az1315-757:06060] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fda0562a1ca]
[fv-az1315-757:06060] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fda0562a28b]
[fv-az1315-757:06060] [11] plumed(+0x134a5)[0x56048dec14a5]
[fv-az1315-757:06060] *** End of error message ***
</pre>
{% endraw %}
