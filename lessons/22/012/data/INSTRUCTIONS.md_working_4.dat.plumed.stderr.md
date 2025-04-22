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
[fv-az2211-783:06110] *** Process received signal ***
[fv-az2211-783:06110] Signal: Aborted (6)
[fv-az2211-783:06110] Signal code:  (-6)
[fv-az2211-783:06110] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f49fc645330]
[fv-az2211-783:06110] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f49fc69eb2c]
[fv-az2211-783:06110] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f49fc64527e]
[fv-az2211-783:06110] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f49fc6288ff]
[fv-az2211-783:06110] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f49fcaa5ff5]
[fv-az2211-783:06110] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f49fcabb0da]
[fv-az2211-783:06110] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f49fcaa5a55]
[fv-az2211-783:06110] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f49fcaa5a6f]
[fv-az2211-783:06110] [ 8] plumed(+0x13209)[0x55895c815209]
[fv-az2211-783:06110] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f49fc62a1ca]
[fv-az2211-783:06110] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f49fc62a28b]
[fv-az2211-783:06110] [11] plumed(+0x134a5)[0x55895c8154a5]
[fv-az2211-783:06110] *** End of error message ***
</pre>
{% endraw %}
