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
[fv-az1690-151:06105] *** Process received signal ***
[fv-az1690-151:06105] Signal: Aborted (6)
[fv-az1690-151:06105] Signal code:  (-6)
[fv-az1690-151:06105] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f963c645330]
[fv-az1690-151:06105] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f963c69eb2c]
[fv-az1690-151:06105] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f963c64527e]
[fv-az1690-151:06105] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f963c6288ff]
[fv-az1690-151:06105] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f963caa5ff5]
[fv-az1690-151:06105] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f963cabb0da]
[fv-az1690-151:06105] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f963caa5a55]
[fv-az1690-151:06105] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f963caa5a6f]
[fv-az1690-151:06105] [ 8] plumed(+0x13209)[0x55da4243c209]
[fv-az1690-151:06105] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f963c62a1ca]
[fv-az1690-151:06105] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f963c62a28b]
[fv-az1690-151:06105] [11] plumed(+0x134a5)[0x55da4243c4a5]
[fv-az1690-151:06105] *** End of error message ***
</pre>
{% endraw %}
