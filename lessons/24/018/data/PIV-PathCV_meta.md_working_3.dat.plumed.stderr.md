Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[fv-az1690-151:05705] *** Process received signal ***
[fv-az1690-151:05705] Signal: Aborted (6)
[fv-az1690-151:05705] Signal code:  (-6)
[fv-az1690-151:05705] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f01eca45330]
[fv-az1690-151:05705] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f01eca9eb2c]
[fv-az1690-151:05705] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f01eca4527e]
[fv-az1690-151:05705] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f01eca288ff]
[fv-az1690-151:05705] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f01ecea5ff5]
[fv-az1690-151:05705] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f01ecebb0da]
[fv-az1690-151:05705] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f01ecea5a55]
[fv-az1690-151:05705] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f01ecea5a6f]
[fv-az1690-151:05705] [ 8] plumed(+0x13209)[0x55bb37c96209]
[fv-az1690-151:05705] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f01eca2a1ca]
[fv-az1690-151:05705] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f01eca2a28b]
[fv-az1690-151:05705] [11] plumed(+0x134a5)[0x55bb37c964a5]
[fv-az1690-151:05705] *** End of error message ***
</pre>
{% endraw %}
