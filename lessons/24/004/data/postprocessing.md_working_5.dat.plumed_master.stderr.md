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
[fv-az1251-633:70115] *** Process received signal ***
[fv-az1251-633:70115] Signal: Aborted (6)
[fv-az1251-633:70115] Signal code:  (-6)
[fv-az1251-633:70115] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fcf9f042520]
[fv-az1251-633:70115] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fcf9f0969fc]
[fv-az1251-633:70115] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fcf9f042476]
[fv-az1251-633:70115] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fcf9f0287f3]
[fv-az1251-633:70115] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fcf9f4a2b9e]
[fv-az1251-633:70115] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fcf9f4ae20c]
[fv-az1251-633:70115] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fcf9f4ae277]
[fv-az1251-633:70115] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fcf9f4ae52b]
[fv-az1251-633:70115] [ 8] plumed_master(+0x14254)[0x55a99921c254]
[fv-az1251-633:70115] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fcf9f029d90]
[fv-az1251-633:70115] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fcf9f029e40]
[fv-az1251-633:70115] [11] plumed_master(+0x14eb5)[0x55a99921ceb5]
[fv-az1251-633:70115] *** End of error message ***
</pre>
{% endraw %}
