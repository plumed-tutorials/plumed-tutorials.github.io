Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[fv-az1690-151:06015] *** Process received signal ***
[fv-az1690-151:06015] Signal: Aborted (6)
[fv-az1690-151:06015] Signal code:  (-6)
[fv-az1690-151:06015] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7994045330]
[fv-az1690-151:06015] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f799409eb2c]
[fv-az1690-151:06015] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f799404527e]
[fv-az1690-151:06015] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f79940288ff]
[fv-az1690-151:06015] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f79944a5ff5]
[fv-az1690-151:06015] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f79944bb0da]
[fv-az1690-151:06015] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f79944a5a55]
[fv-az1690-151:06015] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f79944a5a6f]
[fv-az1690-151:06015] [ 8] plumed(+0x13209)[0x55d5fd426209]
[fv-az1690-151:06015] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f799402a1ca]
[fv-az1690-151:06015] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f799402a28b]
[fv-az1690-151:06015] [11] plumed(+0x134a5)[0x55d5fd4264a5]
[fv-az1690-151:06015] *** End of error message ***
</pre>
{% endraw %}
