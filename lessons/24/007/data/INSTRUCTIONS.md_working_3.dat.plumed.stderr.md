Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1530-405:69483] *** Process received signal ***
[fv-az1530-405:69483] Signal: Aborted (6)
[fv-az1530-405:69483] Signal code:  (-6)
[fv-az1530-405:69483] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe25da42520]
[fv-az1530-405:69483] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe25da969fc]
[fv-az1530-405:69483] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe25da42476]
[fv-az1530-405:69483] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe25da287f3]
[fv-az1530-405:69483] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe25dea2b9e]
[fv-az1530-405:69483] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe25deae20c]
[fv-az1530-405:69483] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe25deae277]
[fv-az1530-405:69483] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe25deae52b]
[fv-az1530-405:69483] [ 8] plumed(+0x12f48)[0x559f4880df48]
[fv-az1530-405:69483] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe25da29d90]
[fv-az1530-405:69483] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe25da29e40]
[fv-az1530-405:69483] [11] plumed(+0x131e5)[0x559f4880e1e5]
[fv-az1530-405:69483] *** End of error message ***
</pre>
{% endraw %}
