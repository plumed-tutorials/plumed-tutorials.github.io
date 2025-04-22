Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label uwall : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az2211-783:06200] *** Process received signal ***
[fv-az2211-783:06200] Signal: Aborted (6)
[fv-az2211-783:06200] Signal code:  (-6)
[fv-az2211-783:06200] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc5b0e45330]
[fv-az2211-783:06200] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc5b0e9eb2c]
[fv-az2211-783:06200] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc5b0e4527e]
[fv-az2211-783:06200] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc5b0e288ff]
[fv-az2211-783:06200] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc5b12a5ff5]
[fv-az2211-783:06200] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc5b12bb0da]
[fv-az2211-783:06200] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc5b12a5a55]
[fv-az2211-783:06200] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc5b12a5a6f]
[fv-az2211-783:06200] [ 8] plumed(+0x13209)[0x562c34f2b209]
[fv-az2211-783:06200] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc5b0e2a1ca]
[fv-az2211-783:06200] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc5b0e2a28b]
[fv-az2211-783:06200] [11] plumed(+0x134a5)[0x562c34f2b4a5]
[fv-az2211-783:06200] *** End of error message ***
</pre>
{% endraw %}
