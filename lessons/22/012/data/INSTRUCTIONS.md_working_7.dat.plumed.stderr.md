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
[fv-az1690-151:06149] *** Process received signal ***
[fv-az1690-151:06149] Signal: Aborted (6)
[fv-az1690-151:06149] Signal code:  (-6)
[fv-az1690-151:06149] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff908c45330]
[fv-az1690-151:06149] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff908c9eb2c]
[fv-az1690-151:06149] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff908c4527e]
[fv-az1690-151:06149] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff908c288ff]
[fv-az1690-151:06149] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff9090a5ff5]
[fv-az1690-151:06149] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff9090bb0da]
[fv-az1690-151:06149] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff9090a5a55]
[fv-az1690-151:06149] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff9090a5a6f]
[fv-az1690-151:06149] [ 8] plumed(+0x13209)[0x55ee58671209]
[fv-az1690-151:06149] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff908c2a1ca]
[fv-az1690-151:06149] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff908c2a28b]
[fv-az1690-151:06149] [11] plumed(+0x134a5)[0x55ee586714a5]
[fv-az1690-151:06149] *** End of error message ***
</pre>
{% endraw %}
