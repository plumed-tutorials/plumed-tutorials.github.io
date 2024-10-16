Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az573-691:04729] *** Process received signal ***
[fv-az573-691:04729] Signal: Aborted (6)
[fv-az573-691:04729] Signal code:  (-6)
[fv-az573-691:04729] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1cc3a42520]
[fv-az573-691:04729] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1cc3a969fc]
[fv-az573-691:04729] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1cc3a42476]
[fv-az573-691:04729] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1cc3a287f3]
[fv-az573-691:04729] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1cc3ea2b9e]
[fv-az573-691:04729] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1cc3eae20c]
[fv-az573-691:04729] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1cc3eae277]
[fv-az573-691:04729] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1cc3eae52b]
[fv-az573-691:04729] [ 8] plumed(+0x12f48)[0x5629fa381f48]
[fv-az573-691:04729] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1cc3a29d90]
[fv-az573-691:04729] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1cc3a29e40]
[fv-az573-691:04729] [11] plumed(+0x131e5)[0x5629fa3821e5]
[fv-az573-691:04729] *** End of error message ***
</pre>
{% endraw %}
