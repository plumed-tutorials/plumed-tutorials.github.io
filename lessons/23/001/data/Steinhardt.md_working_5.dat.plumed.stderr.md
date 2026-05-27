Stderr for source:  Steinhardt.md_working_5.dat   
Download: [zipped raw stdout](Steinhardt.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @1 : action q4 has no component named q4 (hint! the components in this actions are: )
[runnervmg397c:79651] *** Process received signal ***
[runnervmg397c:79651] Signal: Aborted (6)
[runnervmg397c:79651] Signal code:  (-6)
[runnervmg397c:79651] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa085045330]
[runnervmg397c:79651] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa08509eb2c]
[runnervmg397c:79651] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa08504527e]
[runnervmg397c:79651] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa0850288ff]
[runnervmg397c:79651] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa0854a5ff5]
[runnervmg397c:79651] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa0854bb0da]
[runnervmg397c:79651] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa0854a5a55]
[runnervmg397c:79651] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa0854a5a6f]
[runnervmg397c:79651] [ 8] plumed(+0x13209)[0x55f5298f2209]
[runnervmg397c:79651] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa08502a1ca]
[runnervmg397c:79651] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa08502a28b]
[runnervmg397c:79651] [11] plumed(+0x134a5)[0x55f5298f24a5]
[runnervmg397c:79651] *** End of error message ***
</pre>
{% endraw %}
