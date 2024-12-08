Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1778-96:04798] *** Process received signal ***
[fv-az1778-96:04798] Signal: Aborted (6)
[fv-az1778-96:04798] Signal code:  (-6)
[fv-az1778-96:04798] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7faeeb242520]
[fv-az1778-96:04798] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7faeeb2969fc]
[fv-az1778-96:04798] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7faeeb242476]
[fv-az1778-96:04798] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7faeeb2287f3]
[fv-az1778-96:04798] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7faeeb6a2b9e]
[fv-az1778-96:04798] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7faeeb6ae20c]
[fv-az1778-96:04798] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7faeeb6ae277]
[fv-az1778-96:04798] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7faeeb6ae52b]
[fv-az1778-96:04798] [ 8] plumed_master(+0x14254)[0x562c986bf254]
[fv-az1778-96:04798] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7faeeb229d90]
[fv-az1778-96:04798] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7faeeb229e40]
[fv-az1778-96:04798] [11] plumed_master(+0x14eb5)[0x562c986bfeb5]
[fv-az1778-96:04798] *** End of error message ***
</pre>
{% endraw %}
