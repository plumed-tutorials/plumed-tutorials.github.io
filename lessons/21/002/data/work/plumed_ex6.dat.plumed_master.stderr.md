Stderr for source:  work/plumed_ex6.dat   
Download: [zipped raw stdout](plumed_ex6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @53 : keyword ARG is compulsory for this action
[fv-az1272-281:05458] *** Process received signal ***
[fv-az1272-281:05458] Signal: Aborted (6)
[fv-az1272-281:05458] Signal code:  (-6)
[fv-az1272-281:05458] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb620442520]
[fv-az1272-281:05458] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb6204969fc]
[fv-az1272-281:05458] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb620442476]
[fv-az1272-281:05458] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb6204287f3]
[fv-az1272-281:05458] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb6208a2b9e]
[fv-az1272-281:05458] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb6208ae20c]
[fv-az1272-281:05458] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb6208ae277]
[fv-az1272-281:05458] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb6208ae52b]
[fv-az1272-281:05458] [ 8] plumed_master(+0x14254)[0x559725756254]
[fv-az1272-281:05458] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb620429d90]
[fv-az1272-281:05458] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb620429e40]
[fv-az1272-281:05458] [11] plumed_master(+0x14eb5)[0x559725756eb5]
[fv-az1272-281:05458] *** End of error message ***
</pre>
{% endraw %}
