Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @67 : keyword ARG is compulsory for this action
[fv-az1272-281:05277] *** Process received signal ***
[fv-az1272-281:05277] Signal: Aborted (6)
[fv-az1272-281:05277] Signal code:  (-6)
[fv-az1272-281:05277] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f9ed8a42520]
[fv-az1272-281:05277] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f9ed8a969fc]
[fv-az1272-281:05277] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f9ed8a42476]
[fv-az1272-281:05277] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f9ed8a287f3]
[fv-az1272-281:05277] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f9ed8ea2b9e]
[fv-az1272-281:05277] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f9ed8eae20c]
[fv-az1272-281:05277] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f9ed8eae277]
[fv-az1272-281:05277] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f9ed8eae52b]
[fv-az1272-281:05277] [ 8] plumed_master(+0x14254)[0x5651bb5c0254]
[fv-az1272-281:05277] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f9ed8a29d90]
[fv-az1272-281:05277] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f9ed8a29e40]
[fv-az1272-281:05277] [11] plumed_master(+0x14eb5)[0x5651bb5c0eb5]
[fv-az1272-281:05277] *** End of error message ***
</pre>
{% endraw %}
