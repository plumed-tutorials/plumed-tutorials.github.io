Stderr for source:  histograms.md_working_9.dat   
Download: [zipped raw stdout](histograms.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[fv-az1315-757:08071] *** Process received signal ***
[fv-az1315-757:08071] Signal: Aborted (6)
[fv-az1315-757:08071] Signal code:  (-6)
[fv-az1315-757:08071] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0652e45330]
[fv-az1315-757:08071] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0652e9eb2c]
[fv-az1315-757:08071] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0652e4527e]
[fv-az1315-757:08071] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0652e288ff]
[fv-az1315-757:08071] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f06532a5ff5]
[fv-az1315-757:08071] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f06532bb0da]
[fv-az1315-757:08071] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f06532a5a55]
[fv-az1315-757:08071] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f06532a5a6f]
[fv-az1315-757:08071] [ 8] plumed(+0x13209)[0x558f1bb23209]
[fv-az1315-757:08071] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0652e2a1ca]
[fv-az1315-757:08071] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0652e2a28b]
[fv-az1315-757:08071] [11] plumed(+0x134a5)[0x558f1bb234a5]
[fv-az1315-757:08071] *** End of error message ***
</pre>
{% endraw %}
