Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1755-505:05392] *** Process received signal ***
[fv-az1755-505:05392] Signal: Aborted (6)
[fv-az1755-505:05392] Signal code:  (-6)
[fv-az1755-505:05392] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8bc3445330]
[fv-az1755-505:05392] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8bc349eb2c]
[fv-az1755-505:05392] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8bc344527e]
[fv-az1755-505:05392] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8bc34288ff]
[fv-az1755-505:05392] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8bc38a5ff5]
[fv-az1755-505:05392] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8bc38bb0da]
[fv-az1755-505:05392] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8bc38a5a55]
[fv-az1755-505:05392] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8bc38a5a6f]
[fv-az1755-505:05392] [ 8] plumed(+0x13209)[0x561f9b848209]
[fv-az1755-505:05392] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8bc342a1ca]
[fv-az1755-505:05392] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8bc342a28b]
[fv-az1755-505:05392] [11] plumed(+0x134a5)[0x561f9b8484a5]
[fv-az1755-505:05392] *** End of error message ***
</pre>
{% endraw %}
