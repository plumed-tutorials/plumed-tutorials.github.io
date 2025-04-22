Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[fv-az1315-757:06581] *** Process received signal ***
[fv-az1315-757:06581] Signal: Aborted (6)
[fv-az1315-757:06581] Signal code:  (-6)
[fv-az1315-757:06581] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9985845330]
[fv-az1315-757:06581] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f998589eb2c]
[fv-az1315-757:06581] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f998584527e]
[fv-az1315-757:06581] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f99858288ff]
[fv-az1315-757:06581] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9985ca5ff5]
[fv-az1315-757:06581] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9985cbb0da]
[fv-az1315-757:06581] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9985ca5a55]
[fv-az1315-757:06581] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9985ca5a6f]
[fv-az1315-757:06581] [ 8] plumed(+0x13209)[0x55a00a30c209]
[fv-az1315-757:06581] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f998582a1ca]
[fv-az1315-757:06581] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f998582a28b]
[fv-az1315-757:06581] [11] plumed(+0x134a5)[0x55a00a30c4a5]
[fv-az1315-757:06581] *** End of error message ***
</pre>
{% endraw %}
