Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az2211-783:06126] *** Process received signal ***
[fv-az2211-783:06126] Signal: Aborted (6)
[fv-az2211-783:06126] Signal code:  (-6)
[fv-az2211-783:06126] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faefec45330]
[fv-az2211-783:06126] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faefec9eb2c]
[fv-az2211-783:06126] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faefec4527e]
[fv-az2211-783:06126] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faefec288ff]
[fv-az2211-783:06126] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faeff0a5ff5]
[fv-az2211-783:06126] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faeff0bb0da]
[fv-az2211-783:06126] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faeff0a5a55]
[fv-az2211-783:06126] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faeff0a5a6f]
[fv-az2211-783:06126] [ 8] plumed_master(+0x146dd)[0x558c1494c6dd]
[fv-az2211-783:06126] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faefec2a1ca]
[fv-az2211-783:06126] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faefec2a28b]
[fv-az2211-783:06126] [11] plumed_master(+0x15365)[0x558c1494d365]
[fv-az2211-783:06126] *** End of error message ***
</pre>
{% endraw %}
