Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: )
[fv-az1690-151:05641] *** Process received signal ***
[fv-az1690-151:05641] Signal: Aborted (6)
[fv-az1690-151:05641] Signal code:  (-6)
[fv-az1690-151:05641] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc27a445330]
[fv-az1690-151:05641] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc27a49eb2c]
[fv-az1690-151:05641] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc27a44527e]
[fv-az1690-151:05641] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc27a4288ff]
[fv-az1690-151:05641] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc27a8a5ff5]
[fv-az1690-151:05641] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc27a8bb0da]
[fv-az1690-151:05641] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc27a8a5a55]
[fv-az1690-151:05641] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc27a8a5a6f]
[fv-az1690-151:05641] [ 8] plumed(+0x13209)[0x557bd95c8209]
[fv-az1690-151:05641] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc27a42a1ca]
[fv-az1690-151:05641] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc27a42a28b]
[fv-az1690-151:05641] [11] plumed(+0x134a5)[0x557bd95c84a5]
[fv-az1690-151:05641] *** End of error message ***
</pre>
{% endraw %}
