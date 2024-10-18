Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1530-405:69468] *** Process received signal ***
[fv-az1530-405:69468] Signal: Aborted (6)
[fv-az1530-405:69468] Signal code:  (-6)
[fv-az1530-405:69468] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f990f842520]
[fv-az1530-405:69468] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f990f8969fc]
[fv-az1530-405:69468] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f990f842476]
[fv-az1530-405:69468] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f990f8287f3]
[fv-az1530-405:69468] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f990fca2b9e]
[fv-az1530-405:69468] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f990fcae20c]
[fv-az1530-405:69468] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f990fcae277]
[fv-az1530-405:69468] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f990fcae52b]
[fv-az1530-405:69468] [ 8] plumed_master(+0x14254)[0x55674a03b254]
[fv-az1530-405:69468] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f990f829d90]
[fv-az1530-405:69468] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f990f829e40]
[fv-az1530-405:69468] [11] plumed_master(+0x14eb5)[0x55674a03beb5]
[fv-az1530-405:69468] *** End of error message ***
</pre>
{% endraw %}
