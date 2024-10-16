Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(vesselbase/Vessel.cpp:143) void PLMD::vesselbase::Vessel::error(const string&)
ERROR for keyword MORE_THAN in action CLUSTER_DISTRIBUTION with label nclust : could not parse D_0
[fv-az1272-281:04945] *** Process received signal ***
[fv-az1272-281:04945] Signal: Aborted (6)
[fv-az1272-281:04945] Signal code:  (-6)
[fv-az1272-281:04945] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fdd69242520]
[fv-az1272-281:04945] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fdd692969fc]
[fv-az1272-281:04945] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fdd69242476]
[fv-az1272-281:04945] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fdd692287f3]
[fv-az1272-281:04945] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fdd696a2b9e]
[fv-az1272-281:04945] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fdd696ae20c]
[fv-az1272-281:04945] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fdd696ae277]
[fv-az1272-281:04945] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fdd696ae52b]
[fv-az1272-281:04945] [ 8] plumed(+0x12f48)[0x559983b91f48]
[fv-az1272-281:04945] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fdd69229d90]
[fv-az1272-281:04945] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fdd69229e40]
[fv-az1272-281:04945] [11] plumed(+0x131e5)[0x559983b921e5]
[fv-az1272-281:04945] *** End of error message ***
</pre>
{% endraw %}
