Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[fv-az1690-151:06061] *** Process received signal ***
[fv-az1690-151:06061] Signal: Aborted (6)
[fv-az1690-151:06061] Signal code:  (-6)
[fv-az1690-151:06061] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4fdc045330]
[fv-az1690-151:06061] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4fdc09eb2c]
[fv-az1690-151:06061] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4fdc04527e]
[fv-az1690-151:06061] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4fdc0288ff]
[fv-az1690-151:06061] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4fdc4a5ff5]
[fv-az1690-151:06061] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4fdc4bb0da]
[fv-az1690-151:06061] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4fdc4a5a55]
[fv-az1690-151:06061] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4fdc4a5a6f]
[fv-az1690-151:06061] [ 8] plumed(+0x13209)[0x56390bc1e209]
[fv-az1690-151:06061] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4fdc02a1ca]
[fv-az1690-151:06061] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4fdc02a28b]
[fv-az1690-151:06061] [11] plumed(+0x134a5)[0x56390bc1e4a5]
[fv-az1690-151:06061] *** End of error message ***
</pre>
{% endraw %}
