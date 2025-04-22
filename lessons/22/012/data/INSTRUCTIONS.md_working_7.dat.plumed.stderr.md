Stderr for source:  INSTRUCTIONS.md_working_7.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az2211-783:06244] *** Process received signal ***
[fv-az2211-783:06244] Signal: Aborted (6)
[fv-az2211-783:06244] Signal code:  (-6)
[fv-az2211-783:06244] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3247a45330]
[fv-az2211-783:06244] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3247a9eb2c]
[fv-az2211-783:06244] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3247a4527e]
[fv-az2211-783:06244] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3247a288ff]
[fv-az2211-783:06244] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3247ea5ff5]
[fv-az2211-783:06244] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3247ebb0da]
[fv-az2211-783:06244] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3247ea5a55]
[fv-az2211-783:06244] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3247ea5a6f]
[fv-az2211-783:06244] [ 8] plumed(+0x13209)[0x55f621785209]
[fv-az2211-783:06244] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3247a2a1ca]
[fv-az2211-783:06244] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3247a2a28b]
[fv-az2211-783:06244] [11] plumed(+0x134a5)[0x55f6217854a5]
[fv-az2211-783:06244] *** End of error message ***
</pre>
{% endraw %}
