Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[fv-az1778-96:05898] *** Process received signal ***
[fv-az1778-96:05898] Signal: Aborted (6)
[fv-az1778-96:05898] Signal code:  (-6)
[fv-az1778-96:05898] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ffb14242520]
[fv-az1778-96:05898] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ffb142969fc]
[fv-az1778-96:05898] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ffb14242476]
[fv-az1778-96:05898] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ffb142287f3]
[fv-az1778-96:05898] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ffb146a2b9e]
[fv-az1778-96:05898] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ffb146ae20c]
[fv-az1778-96:05898] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ffb146ae277]
[fv-az1778-96:05898] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ffb146ae52b]
[fv-az1778-96:05898] [ 8] plumed(+0x12f48)[0x563fabe10f48]
[fv-az1778-96:05898] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ffb14229d90]
[fv-az1778-96:05898] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ffb14229e40]
[fv-az1778-96:05898] [11] plumed(+0x131e5)[0x563fabe111e5]
[fv-az1778-96:05898] *** End of error message ***
</pre>
{% endraw %}
