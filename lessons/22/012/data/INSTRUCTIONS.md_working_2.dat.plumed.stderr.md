Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[fv-az1429-301:04289] *** Process received signal ***
[fv-az1429-301:04289] Signal: Aborted (6)
[fv-az1429-301:04289] Signal code:  (-6)
[fv-az1429-301:04289] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f603f842520]
[fv-az1429-301:04289] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f603f8969fc]
[fv-az1429-301:04289] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f603f842476]
[fv-az1429-301:04289] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f603f8287f3]
[fv-az1429-301:04289] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f603fca2b9e]
[fv-az1429-301:04289] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f603fcae20c]
[fv-az1429-301:04289] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f603fcae277]
[fv-az1429-301:04289] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f603fcae52b]
[fv-az1429-301:04289] [ 8] plumed(+0x12f48)[0x55d09f0b3f48]
[fv-az1429-301:04289] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f603f829d90]
[fv-az1429-301:04289] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f603f829e40]
[fv-az1429-301:04289] [11] plumed(+0x131e5)[0x55d09f0b41e5]
[fv-az1429-301:04289] *** End of error message ***
</pre>
{% endraw %}