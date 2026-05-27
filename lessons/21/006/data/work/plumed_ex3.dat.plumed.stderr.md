Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[runnervmg397c:79536] *** Process received signal ***
[runnervmg397c:79536] Signal: Aborted (6)
[runnervmg397c:79536] Signal code:  (-6)
[runnervmg397c:79536] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1d99245330]
[runnervmg397c:79536] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1d9929eb2c]
[runnervmg397c:79536] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1d9924527e]
[runnervmg397c:79536] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1d992288ff]
[runnervmg397c:79536] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1d996a5ff5]
[runnervmg397c:79536] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1d996bb0da]
[runnervmg397c:79536] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1d996a5a55]
[runnervmg397c:79536] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1d996a5a6f]
[runnervmg397c:79536] [ 8] plumed(+0x13209)[0x560d865a5209]
[runnervmg397c:79536] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1d9922a1ca]
[runnervmg397c:79536] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1d9922a28b]
[runnervmg397c:79536] [11] plumed(+0x134a5)[0x560d865a54a5]
[runnervmg397c:79536] *** End of error message ***
</pre>
{% endraw %}
