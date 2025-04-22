Stderr for source:  Behler.md_working_4.dat   
Download: [zipped raw stdout](Behler.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1315-757:07091] *** Process received signal ***
[fv-az1315-757:07091] Signal: Aborted (6)
[fv-az1315-757:07091] Signal code:  (-6)
[fv-az1315-757:07091] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7332845330]
[fv-az1315-757:07091] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f733289eb2c]
[fv-az1315-757:07091] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f733284527e]
[fv-az1315-757:07091] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f73328288ff]
[fv-az1315-757:07091] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7332ca5ff5]
[fv-az1315-757:07091] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7332cbb0da]
[fv-az1315-757:07091] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7332ca5a55]
[fv-az1315-757:07091] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7332ca5a6f]
[fv-az1315-757:07091] [ 8] plumed(+0x13209)[0x55b120226209]
[fv-az1315-757:07091] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f733282a1ca]
[fv-az1315-757:07091] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f733282a28b]
[fv-az1315-757:07091] [11] plumed(+0x134a5)[0x55b1202264a5]
[fv-az1315-757:07091] *** End of error message ***
</pre>
{% endraw %}
