Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @49 : keyword ARG is compulsory for this action
[fv-az1429-301:05131] *** Process received signal ***
[fv-az1429-301:05131] Signal: Aborted (6)
[fv-az1429-301:05131] Signal code:  (-6)
[fv-az1429-301:05131] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd5e6e42520]
[fv-az1429-301:05131] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd5e6e969fc]
[fv-az1429-301:05131] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd5e6e42476]
[fv-az1429-301:05131] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd5e6e287f3]
[fv-az1429-301:05131] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd5e72a2b9e]
[fv-az1429-301:05131] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd5e72ae20c]
[fv-az1429-301:05131] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd5e72ae277]
[fv-az1429-301:05131] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd5e72ae52b]
[fv-az1429-301:05131] [ 8] plumed_master(+0x14254)[0x56249c8a2254]
[fv-az1429-301:05131] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd5e6e29d90]
[fv-az1429-301:05131] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd5e6e29e40]
[fv-az1429-301:05131] [11] plumed_master(+0x14eb5)[0x56249c8a2eb5]
[fv-az1429-301:05131] *** End of error message ***
</pre>
{% endraw %}
