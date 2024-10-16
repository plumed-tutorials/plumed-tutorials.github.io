Stderr for source:  postprocessing.md_working_5.dat   
Download: [zipped raw stdout](postprocessing.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @18 : keyword ARG is compulsory for this action
[fv-az1020-199:04804] *** Process received signal ***
[fv-az1020-199:04804] Signal: Aborted (6)
[fv-az1020-199:04804] Signal code:  (-6)
[fv-az1020-199:04804] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f828a842520]
[fv-az1020-199:04804] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f828a8969fc]
[fv-az1020-199:04804] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f828a842476]
[fv-az1020-199:04804] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f828a8287f3]
[fv-az1020-199:04804] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f828aca2b9e]
[fv-az1020-199:04804] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f828acae20c]
[fv-az1020-199:04804] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f828acae277]
[fv-az1020-199:04804] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f828acae52b]
[fv-az1020-199:04804] [ 8] plumed_master(+0x14254)[0x55d46f108254]
[fv-az1020-199:04804] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f828a829d90]
[fv-az1020-199:04804] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f828a829e40]
[fv-az1020-199:04804] [11] plumed_master(+0x14eb5)[0x55d46f108eb5]
[fv-az1020-199:04804] *** End of error message ***
</pre>
{% endraw %}
