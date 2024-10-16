Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label @s9 : keyword SIGMA could not be read correctly
[fv-az573-691:04360] *** Process received signal ***
[fv-az573-691:04360] Signal: Aborted (6)
[fv-az573-691:04360] Signal code:  (-6)
[fv-az573-691:04360] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f59bb442520]
[fv-az573-691:04360] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f59bb4969fc]
[fv-az573-691:04360] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f59bb442476]
[fv-az573-691:04360] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f59bb4287f3]
[fv-az573-691:04360] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f59bb8a2b9e]
[fv-az573-691:04360] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f59bb8ae20c]
[fv-az573-691:04360] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f59bb8ae277]
[fv-az573-691:04360] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f59bb8ae52b]
[fv-az573-691:04360] [ 8] plumed_master(+0x14254)[0x5627d20b4254]
[fv-az573-691:04360] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f59bb429d90]
[fv-az573-691:04360] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f59bb429e40]
[fv-az573-691:04360] [11] plumed_master(+0x14eb5)[0x5627d20b4eb5]
[fv-az573-691:04360] *** End of error message ***
</pre>
{% endraw %}
