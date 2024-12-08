Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1778-96:04790] *** Process received signal ***
[fv-az1778-96:04790] Signal: Aborted (6)
[fv-az1778-96:04790] Signal code:  (-6)
[fv-az1778-96:04790] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0c4b642520]
[fv-az1778-96:04790] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f0c4b6969fc]
[fv-az1778-96:04790] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0c4b642476]
[fv-az1778-96:04790] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f0c4b6287f3]
[fv-az1778-96:04790] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f0c4baa2b9e]
[fv-az1778-96:04790] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f0c4baae20c]
[fv-az1778-96:04790] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f0c4baae277]
[fv-az1778-96:04790] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f0c4baae52b]
[fv-az1778-96:04790] [ 8] plumed(+0x12f48)[0x5633c4496f48]
[fv-az1778-96:04790] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0c4b629d90]
[fv-az1778-96:04790] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0c4b629e40]
[fv-az1778-96:04790] [11] plumed(+0x131e5)[0x5633c44971e5]
[fv-az1778-96:04790] *** End of error message ***
</pre>
{% endraw %}
