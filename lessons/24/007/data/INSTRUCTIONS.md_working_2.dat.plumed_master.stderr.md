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
[fv-az1778-96:04774] *** Process received signal ***
[fv-az1778-96:04774] Signal: Aborted (6)
[fv-az1778-96:04774] Signal code:  (-6)
[fv-az1778-96:04774] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fdd54242520]
[fv-az1778-96:04774] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fdd542969fc]
[fv-az1778-96:04774] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fdd54242476]
[fv-az1778-96:04774] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fdd542287f3]
[fv-az1778-96:04774] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fdd546a2b9e]
[fv-az1778-96:04774] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fdd546ae20c]
[fv-az1778-96:04774] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fdd546ae277]
[fv-az1778-96:04774] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fdd546ae52b]
[fv-az1778-96:04774] [ 8] plumed_master(+0x14254)[0x55bbcc1ee254]
[fv-az1778-96:04774] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fdd54229d90]
[fv-az1778-96:04774] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fdd54229e40]
[fv-az1778-96:04774] [11] plumed_master(+0x14eb5)[0x55bbcc1eeeb5]
[fv-az1778-96:04774] *** End of error message ***
</pre>
{% endraw %}